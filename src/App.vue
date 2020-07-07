<template>
  <div id="app">
    <ProductListOne v-bind:products="products" />
    <ProductListTwo v-bind:products="products" />
    <!-- <router-view/> -->
  </div>
</template>

<script>
import ProductListOne from './components/productListOne';
import ProductListTwo from './components/productListTwo';

export default {
  components: {
    'ProductListOne': ProductListOne,
    'ProductListTwo': ProductListTwo
  },
  name: 'app',
  data() {
    return {
      products: [
        {name: 'Banana Skin', price: 20},
        {name: 'Shiny Star', price: 40},
        {name: 'Green Shells', price: 60},
        {name: 'Red Shells', price: 80}
      ]
    }
  }
};
</script>

<style lang="scss">

</style>
