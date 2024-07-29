<template>
    <div>
        <h2> Product details for {{ id }}</h2>
        <p>{{ product.title }}</p>
    </div>
</template>

<script setup lang="ts">
    const { id } = useRoute().params
    const url = "https://fakestoreapi.com/products/" + id
    const {data: product} = await useFetch(url);

    definePageMeta({
        layout: 'product'
    })
    

</script>

<style scoped>

</style>

