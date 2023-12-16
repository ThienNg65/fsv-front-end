<template>
  <div v-if="products.length > 0">
    <ProductsListItem
      v-for="product in products"
      v-on:remove-from-cart="$emit('remove-from-cart', $event)"
      :key="product.id"
      :product="product"
    />
  </div>
  <p v-else>You haven't added anything to your cart yet!</p>
</template>

<script>
import ProductsListItem from './ProductsListItem.vue'
export default {
  name: 'ProductsList',
  props: ['products'],
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
