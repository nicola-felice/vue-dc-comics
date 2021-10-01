<template>

  <div id="current_series_comics">
    <div class="container">
      <div class="label_current_series">current series</div>

      <ul class="comics_list">
        <Product v-for="(elm, index) in comicsList" :key="index" :product-data="elm" />
      </ul>

      <button class="load_more_btn">load more</button>
    </div>
  </div>

</template>


<script>
// components
import Product from "./Product.vue";
// data 
import json from "../assets/dc-comics.json";

export default {
  name: 'ComicsSeries',
  components: {
    Product,
  },
  data() {
    return {
      comicsList: json,
    }
  }
}
</script>


<style lang="scss" scoped>
@import "../assets/variables.scss";

#current_series_comics {
  background-color: #1c1c1c;
  color: white;

  .container {
    position: relative;
    display: flex;
    flex-direction: column;
  }

  // label current series
  .label_current_series {
    background-color: $main_color;
    display: inline-block;
    padding: .5rem 1.25rem;
    font-size: 1.35rem;
    text-transform: uppercase;
    font-weight: bold;
    position: absolute;
    top: 0;
    transform: translateY(-50%);
    left: 0;
  }

  // button load more
  .load_more_btn {
    background-color: $main_color;
    border: transparent;
    padding: .5rem 2rem;
    font-size: .9rem;
    color: white;
    margin: auto;
    margin-bottom: 1.5rem;
    text-transform: uppercase;
    cursor: pointer;
  }

  // list of comics
  .comics_list {
    display: flex;
    flex-wrap: wrap;
    padding: 2.5rem 0;
  }
}
</style>