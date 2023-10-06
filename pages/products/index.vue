<template>
    <div class="grid grid-cols-4 gap-5">
        <div v-for="item in products">
            <Card :product="item" />
        </div>
    </div>
</template>

<script setup>
    definePageMeta({
        layout: 'products'
    })

    const { data: products } = await useFetch('https://fakestoreapi.com/products')
</script>

<style scoped>

h2 {
    font-size: 2.25rem;
    
}
</style>