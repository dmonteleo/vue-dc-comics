<template>
  <main>
    <h3>Lista Prodotti</h3>
    <div class="container cards-container">
      <ProductCard
        v-for="(productItem, index) in productList" 
        :key="index"
        :productData="productItem"
      />
    </div>
  </main>
</template>

<script>
import ProductCard from './ProductCard.vue';
import productsCards from '../assets/data/productsCards';
export default {
  name: 'MainComponent', 
  components: { 
    ProductCard 
    },
  data() {
    return {
      productList: productsCards
    }
  }
}
</script>

<style lang="scss" scoped>
@import '../assets/style/_vars.scss';
main {
  text-align: center; 
  padding: 30px;
  background-image: url('../assets/sfondo-cibo-2.jpg');
  min-height: 500px;
  h3 {
    color: $primary-color;
    margin-bottom: 3rem;
  }
  .cards-container {
    display: flex;
    flex-wrap: wrap; 
  }
}


</style>