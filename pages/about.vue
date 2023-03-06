<template>
    <div>
        <h2>About</h2>
        <p>
            Lorem ipsum dolor sit amet, consectetur adipisicing elit. Aperiam, aspernatur atque cum cumque dolores eius esse facilis, illo ipsa laboriosam molestias natus placeat quod rem sequi temporibus unde velit voluptate.
        </p>
        <p>{{ data }}</p>
    </div>
</template>

<script setup>
const { data } = await useFetch('/api/currency/GBP')
</script>
