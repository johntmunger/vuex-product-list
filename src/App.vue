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

    }
  }
};
</script>

<style lang="scss">

</style>
