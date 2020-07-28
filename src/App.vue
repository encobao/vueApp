<template src="./App.html"></template>

<script>
import ProductList from './components/ProductList.vue'

export default {
  name: 'App',
  data() { 
    return { 
      products: [
        { id:1, name: 'product name from app component', price: 3.5, img_src: 'http://192.168.0.17/images/set1.jpg' },
        { id:2, name: 'product1 name from app component', price: 2.51, img_src: 'http://192.168.0.17/images/set2.jpg' }
      ]
    }
  },
  components: {
    ProductList
  },
  methods: {
    addToCart(productId, quantity) {
      alert('adding ' + quantity + ' products to cart ID: ' + productId);
    }
  }
}
</script>

<style src="./App.css"></style>
