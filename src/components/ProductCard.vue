<template>
  <div>
    <img :src="productData.src" :alt="productData.titolo">
    <h3>{{productData}}</h3>
  </div>
</template>

<script>
export default {
  name: 'ProductCard',
  props: {
    productData: Object
  }

}
</script>

<style lang="scss" scoped>
@import '../assets/style/_vars.scss';
div {
  flex-basis: 25%;
  background-color: white;
  border: 2px solid lighten($color: $primary-color, $amount: 70%);
  padding: 1rem;
  h3 {
    color: $primary-color;
  }
}

</style>