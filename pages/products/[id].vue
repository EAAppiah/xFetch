<template>
  <div>
    <CardDetails :product="item" />
  </div>
</template>

<script setup>
const { id } = useRoute().params;
const uri = 'https://fakestoreapi.com/products/' + id  


  //fetch the product
  const { data: item } = await useFetch(uri)


definePageMeta({
        layout: 'products'
    })
</script>

<style scoped>


</style>
