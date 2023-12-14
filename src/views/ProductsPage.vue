<template>
  <div id="page-wrap">
    <ProductsGrid :products="products" />
  </div>
</template>

<script>
import axios from 'axios'
import ProductsGrid from '../components/ProductsGrid/ProductsGrid.vue'
export default {
  name: 'ProductsPage',
  components: { ProductsGrid },
  data() {
    return {
      products: []
    }
  },
  async created() {
    try {
      const result = await axios.get('/api/products')
      const products = result.data
      this.products = products
    } catch (error) {
      console.error('Error fetching products:', error)
    }
  }
}
</script>
