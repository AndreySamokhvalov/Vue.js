
<template>
  <div>
    <ProductDetails class="product__card"
        v-for="product in products" 
        :key="product.id"
        :product="product"/>
  </div>
</template>

<script>
import ProductDetails from '@/components/ProductDetails.vue';
export default {
  name: "ProductList",
  components: { ProductDetails },
  data() {
    return {
      products:
        [
          { id: '1', name: 'Red pen', price: 14, available: true },
          { id: '2', name: 'Blue pen', price: 21, available: true },
          { id: '3', name: 'Green pen', price: 9, available: false },
          { id: '4', name: 'Black pen', price: 20, available: true }]
    };
  },

  computed: {
    formattedPrice: function (id) {
      console.log(id);
     const obj = JSON.parse(JSON.stringify(this.products[id]));
     console.log(obj);
      console.log(obj.price);
      return `$${obj.price}`;
    }
  }
}
</script>

<style scoped lang="css">
.product__card{
  display: flex;
    width: 170px;
    height: 170px;
    border: 1px solid #929292;
    border-radius: 12px;
    margin-bottom: 12px;
    flex-direction: row;
    flex-wrap: wrap;
    justify-content: center;
    align-items: flex-start;
    background-color: beige;

}
</style>