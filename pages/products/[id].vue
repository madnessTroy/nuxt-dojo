<template>
    <div>
        <ProductDetail :product="product" />
    </div>
</template>

<script setup>
const { id } = useRoute().params
const url = 'https://fakestoreapi.com/products/' + id

const { data: product } = await useFetch(url, { key: id })

if (!product.value) {
    throw createError({
        status: 404,
        statusMessage: `Product not found: ${id}`,
        fatal: true
    })
}

definePageMeta({
    layout: 'products'
})
</script>
