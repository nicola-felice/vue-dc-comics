<template>
  <li class="product">
    <div class="image_wrapper">
      <img :src="productData.thumb" alt="productData.type">
    </div>
    <span>{{productData.series}}</span>
  </li>
</template>


<script>
export default {
  name: 'Product',
  props: ['productData'],
}
</script>


<style lang="scss" scoped>
.product {
  width: calc(100% / 6);
  list-style: none;
  text-transform: uppercase;
  font-size: .9rem;
  padding: .75rem;

  .image_wrapper {
    position: relative;
    height: 0;
    padding-bottom: 100%;
    margin-bottom: .7rem;

    img {
      position: absolute;
      width: 100%;
      height: 100%;
      object-fit: cover;
      object-position: top;
    }
  }
}
</style>