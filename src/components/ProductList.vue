<template>

	<div class="product_list">

			<div v-for="product in items" :key="product.id" class="product">
					
          <div class="col1">
						<img class="product_image" :src="product.img_src" />
					</div> 

					<div class="col2">
            <div class="name">
                {{ product.name }}
            </div>

            <div class="price">
              ${{ product.price.toFixed(2) }} 
            </div>

            <div class="addToCart_form">
              
              <form @submit="addProductToCart">
                
                <input type="hidden" :value="product.id" id="productId">
                <select class="quantity_selector" id="quantity">
                  <option v-for="n in 30" :key="n" :value="n">{{ n }}</option>
                </select>
                <button class="addButton" type="submit" >Add to cart</button>

              </form>

            </div>
					</div>

			</div>

	</div>

</template>

<script>

export default {
  name: 'ProductList',
  props: {
    items: {
      type: Array,
      required: true
    }
  },
  methods: {
    addProductToCart(event) {
      event.preventDefault();
      let prodId = event.currentTarget.elements.namedItem('productId').value;
      let quant = event.currentTarget.elements.namedItem('quantity').value;
      this.$emit('addToCart', prodId, quant);
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

.col1 {
  display: block;
}

.col2 {
  display: block;
}

.product {
	--test_border: 1px solid black;  
  --test_border: none;
  
  color: #5a5a5a;
	font-family: Arial, Helvetica, sans-serif;

  
  display: grid;
  grid-template-columns: 50% auto;
  background-color: white;
  border-radius: 11px;
  box-shadow: 0px 3px 8px rgb(194, 194, 194);
  padding: 20px;
	margin-bottom: 20px;
}
  
.product > div {
	padding: 10px;
	border: var(--test_border);
}

.name {
  font-size: 0.9rem;
  margin-bottom: 10px;
}
  
.price {
	/*font-weight: bold;*/
	font-size: 1.1rem;
  margin-bottom: 10px;
}
  
.addToCart_form {
	font-size: 1.2rem;
  margin-bottom: 10px;
}
  
.quantity_selector {
	display: block;
  color: rgb(99, 99, 99);
  border: 1px solid rgb(197, 194, 194);
	padding: 3px 10px;
	font-size: 1rem;
	background-color: white;
  border-radius: 5px;
}

.addButton {
	display: block;
  font-size: 0.9rem;
  color: rgb(97, 97, 97);
  background-color: rgb(255, 255, 255);
	padding: 6px 20px;
  border: 2px solid rgb(131, 131, 131);
  border-radius: 4px;
  margin: 15px 0;
}

.product_image {
  width: 100%;
}

</style>
