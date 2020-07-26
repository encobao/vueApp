<template src="./App.html"></template>

<script>
import ProductList from './components/ProductList.vue'

export default {
  name: 'App',
  /*
  data() { 
      return { 
          IMAGES_URL: process.env.VUE_APP_IMAGES_URL,
          products: [
            { id:1, name: 'product name from app component', price: 1.50, img_src: 'set1.jpg' },
            { id:2, name: 'product1 name from app component', price: 2.51, img_src: 'set2.jpg' }
          ]
      }
  },
  */
  components: {
    ProductList
  }
}
</script>

<style src="./App.css"></style>
