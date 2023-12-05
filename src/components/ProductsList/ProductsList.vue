<template>
  <ProductsListItem v-for="product in cartItems" :key="product.id" :product="product" />
</template>

<script>
import ProductsListItem from './ProductsListItem.vue'
export default {
  name: 'ProductsList',
  props: ['cartItems'],
  components: { ProductsListItem }
}
</script>

<style scoped>
.product-container {
  align-content: 'center';
  border-bottom: 1px solid #ddd;
  display: flex;
  padding: 16px;
  width: 100%;
}
</style>
