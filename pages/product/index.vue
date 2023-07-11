<template>
  <div>
    <div class="grid grid-cols-4 gap-5">
      <div v-for="p in product">
        <ProductCard :product="p" />
      </div>
    </div>
  </div>
</template>

<script setup>
  //  fetch the products
  const { data: product } = await useFetch('https://fakestoreapi.com/products')

  definePageMeta({
    layout: "product",
  })

  useHead({
    title: 'Nuxt Doja | Merch',
    meta: [
      { name: 'description', content: 'Nuxt 3 Merch'}
    ]
  })
</script>