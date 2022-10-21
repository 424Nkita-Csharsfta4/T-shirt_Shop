<template>
    <div class="v-cart">
        <router-link :to="{name: 'catalog'}">
      <div class="v-catalog__link_to_cart">Back to Catalog</div>
    </router-link>
    <h1>Cart</h1>
    <p v-if="!cart_data.length">There are no products in cart...</p>
    <div class="v-cart__total">
      <p class="total__name">Total:</p>
      <p>{{cartTotalCost | toFix | formattedPrice}}</p>
    </div>
    </div>
</template>
<script>
export default{
    name: "v-cart",
    components: {
      vCartItem
    },
    props: {
      cart_data: {
        type: Array,
        default() {
          return []
        }
      }
    },
    data() {
      return {}
    },
    computed: {
      cartTotalCost() {
        let result = []
        if (this.cart_data.length) {
          for (let item of this.cart_data) {
            result.push(item.price * item.quantity)
          }
          result = result.reduce(function (sum, el) {
            return sum + el;
          })
          return result;
        } else {
          return 0
        }
      }
    }
  }

</script>
<style>

</style>