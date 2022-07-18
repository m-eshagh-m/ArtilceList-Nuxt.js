<template>
  <div>
    <h1>Products list</h1>
    <ProductsList :products="products" />
  </div>
</template>

<script>
import axios from 'axios'

export default {
  async asyncData() {
    const { data } = await axios.get('https://fakestoreapi.com/products/')
    return { products: data }
  },
}
</script>
