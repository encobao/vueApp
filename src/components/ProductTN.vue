<template>
			<div class="product">

					<div class="col1">
						<img class="product_image" :src="img_src" />
					</div> 

					<div class="col2">
            <div class="name">
                {{ name }}
            </div>

            <div class="price">
              ${{ price.toFixed(2) }} 
            </div>

            <div class="addToCart_form">
              <form>
                <select class="quantity_selector">
                  <option value=1>1</option>
                  <option value=2>2</option>
                  <option value=3>3</option>
                  <option value=4>4</option>
                  <option value=5>5</option>
                  <option value=6>6</option>
                  <option value=7>7</option>
                  <option value=8>8</option>
                  <option value=9>9</option>
                  <option value=10>10</option>
                  <option value=11>11</option>
                  <option value=12>12</option>
                  <option value=13>13</option>
                  <option value=14>14</option>
                  <option value=15>15</option>
                  <option value=16>16</option>
                  <option value=17>17</option>
                  <option value=18>18</option>
                  <option value=19>19</option>
                  <option value=20>20</option>
                  <option value=21>21</option>
                  <option value=22>22</option>
                  <option value=23>23</option>
                  <option value=24>24</option>
                  <option value=25>25</option>
                  <option value=26>26</option>
                  <option value=27>27</option>
                  <option value=28>28</option>
                  <option value=29>29</option>
                  <option value=30>30</option>
                </select>

                <button class="addButton" type="submit" >Add to cart</button>
              </form>
            </div>
					</div>

			</div>
</template>

<script>
export default {
  name: 'ProductTN',
  props: {
      img_src:  String, 
      name:     String,
      price:    Number
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
  border: 2px solid rgb(65, 65, 65);
  border-radius: 4px;
  margin: 15px 0;
}

.product_image {
  width: 100%;
}
</style>
