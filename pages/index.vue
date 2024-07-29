<template>
    <div>
        <h2>Products</h2>
        <div v-for="p in products" :key="p.id">
            <ProductCard :product="p"/>
        </div>
    </div>
</template>

<script setup lang="ts">
    interface Product {
        id: number;
        title: string
    }

    definePageMeta({
        layout: 'product'
    });

    const { data: products } = await useFetch<Product[]>('https://fakestoreapi.com/products');
</script>

<style scoped>
h2 {
    margin-bottom: 20px;
    font-size: 36px;
}

p {
    margin: 20px 0;
}
</style>
