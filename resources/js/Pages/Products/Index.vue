<script setup>
defineProps({
    products: {
        type: Array,
        required: true,
    },
});
</script>

<template>
    <div class="container">
        <h1>Каталог товаров</h1>

        <div class="grid">
            <article
                v-for="product in products"
                :key="product.id"
                class="card"
            >
            <img
                class="card-image"
                :src="product.image_path"
                :alt="product.title"
            />

            <h2 class="card-title">{{ product.title }}</h2>

            <p class="card-price">{{ product.price }} ₽</p>

            <p class="card-stock">
                На складе: {{ product.stock }} шт.
            </p>
            </article>
        </div>
    </div>
</template>