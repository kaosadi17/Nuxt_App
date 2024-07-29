<template>
    <div>
        <img :src="product.image" alt="product img">
        <p>{{ product.title }}</p>
        <NuxtLink :to="`/products/${product.id}`">View Details</NuxtLink>
    </div>
</template>

<script setup>
    const { product } = defineProps(['product'])
</script>

<style scoped>
    img{
        width: 100px;
        height: 100px;
    }
</style>
