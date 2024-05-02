<template>
    <div>

        <Head>
            <Title>Nuxt Basic | {{ product.title }}</Title>
            <Meta name="description" :content="product.description" />
        </Head>
        <ProductDetails :product="product"></ProductDetails>
    </div>
</template>

<script setup>
import ProductDetails from '~/components/ProductDetails.vue';

const { id } = useRoute().params
const uri = 'https://fakestoreapi.com/products/' + id
//fetch the product
const { data: product } = await useFetch(uri, { key: id })
definePageMeta({
    layout: 'products'
})
if (!product.value) {
    throw createError({ statusCode: 404, statusMessage: "product not found", fatal: true })
}
</script>

<style scoped>
.thumb {
    max-height: 120px;
    max-width: 70%;
    margin: 0 auto;
}
</style>