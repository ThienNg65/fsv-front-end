import { products } from '../fake-data'; import ProductsGridItem from './ProductsGridItem.vue';
<template>
  <div class="grid-wrap">
    <ProductsGridItem v-for="product in products" :key="product.id" :product="product">
    </ProductsGridItem>
  </div>
</template>

<script>
import ProductsGridItem from './ProductsGridItem.vue'
export default {
  name: 'ProductsGrid',
  props: ['products'],
  components: {
    ProductsGridItem
  }
}
</script>

<style scoped>
.grid-wrap {
  display: flex;
  flex-wrap: wrap;
  justify-content: space-between;
  margin-top: 16px;
}
</style>
