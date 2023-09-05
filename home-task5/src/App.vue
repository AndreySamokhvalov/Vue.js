<template>
  <div id="app">
    <ProductList />
  </div>
</template>

<script>

import ProductList from './components/ProductList.vue';

export default {
  name: 'App',
  components: {
    ProductList
  }
}
</script>

<style>
#app{
  display: flex;
    flex-direction: column;
    flex-wrap: nowrap;
    align-items: center;
    justify-content: center;
}

</style>
