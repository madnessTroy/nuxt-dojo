<template>
    <div>
        <div class="grid grid-cols-4 gap-5" v-if="products">
            <div v-for="p in products">
                <ProductCard :product="p" />
            </div>
        </div>
    </div>
</template>

<script setup>
definePageMeta({
    layout: 'products'
})
const url = 'https://fakestoreapi.com/products'

const { data: products } = await useFetch(url)

useHead({
    title: 'Nuxt Dojo | Merch',
    meta: [
        { name: 'description', content: 'Nuxt 3 Merch' }
    ]
})
</script>
