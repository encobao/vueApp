<template>
	<div class="product_list">
        <ProductTN
                v-for="product in products"      
                :key="product.id"
                :name="product.name"
                :price="product.price"
                :img_src="IMAGES_URL + product.img_src"
        />
	</div>
</template>

<script>
import ProductTN from './ProductTN.vue'

export default {
  name: 'ProductList',
  data() { 
      return { 
          IMAGES_URL: process.env.VUE_APP_IMAGES_URL,
          products: [
            { id:1, name: 'product name from app component', price: 1.50, img_src: 'set1.jpg' },
            { id:2, name: 'product1 name from app component', price: 2.51, img_src: 'set2.jpg' }
          ]
      }
  },
  components: {
    ProductTN
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
</style>
