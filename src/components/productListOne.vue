<template>
  <div id="product-list-one">
    <h3>Product List One</h3>
    <ul>
      <li v-for="product in saleProducts" :key="product.name">
        <span class="name">{{product.name}}</span>
        <span class="name">${{product.price}}</span>
      </li>
    </ul>
    <!-- Pass an amount parameter through the click event $4 below -->
    <button v-on:click="reducePrice">Reduce Price</button>
  </div>
</template>

<script>
export default {
  name: 'ProductListOne',
  computed: {
    products() {
      return this.$store.state.products;
    },
    saleProducts() {
      return this.$store.getters.saleProducts;
    }
  },
  methods: {
    // Try to avoid 'commit' here, use dispatch to the action instead
    reducePrice: function() {
      this.$store.dispatch('reducePrice');
    }
  }
}
</script>

<style scoped>
#product-list-one{
    background: #FFF8B1;
    box-shadow: 1px 2px 3px rgba(0,0,0,0.2);
    margin-bottom: 30px;
    padding: 10px 20px;
}
#product-list-one ul{
    padding: 0;
}
#product-list-one li{
    display: inline-block;
    margin-right: 10px;
    margin-top: 10px;
    padding: 20px;
    background: rgba(255,255,255,0.7);
}
.price{
    font-weight: bold;
    color: #E8800C;
}
</style>