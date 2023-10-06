<template>
    <div class="card text-center">
        <img :src="product.image" alt="product img" class="product__card">
        <p class="font-bold text-gray-500 m-4 truncate">{{ product.title }}</p>
        <NuxtLink :to="`/products/${product.id}`">
            <p class="btn my-4">View Details</p>
        </NuxtLink>
    </div>
</template>

<script setup>

    const { product } = defineProps(['product'])

</script>

<style scoped>

    img {
        transition: transform 0.3s ease;
    }

    img:hover {
        transform: scale(1.1);
    }

    .product__card {
        max-height: 120px;
        max-width: 70%;
        margin: 0 auto;
    }
</style>