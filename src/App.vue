<template>
  <div id="app">

    <Header/>

    <main>
      <div id="hero"></div>

      <div id="currentSeriesComics">
        <div class="container">
          <div class="label_current_series">current series</div>

          <ul class="comics_list">
            <Product v-for="(elm, index) in comicsList" :key="index" :product-data="elm" />
          </ul>

          <button class="load_more_btn">load more</button>
        </div>
      </div>

      <BuyComicsBanner/>
    </main>

    <Footer/>

  </div>
</template>


<script>
// components
import Header from "./components/Header.vue";
import Footer from "./components/Footer.vue";
import BuyComicsBanner from "./components/BuyComicsBanner.vue";
import Product from "./components/Product.vue";
// data 
import json from "./assets/dc-comics.json";

export default {
  name: 'App',
  components: {
    Header,
    Footer,
    BuyComicsBanner,
    Product
  }, 
  data() {
    return {
      comicsList: json,
    }
  }
}

</script>


<style lang="scss">
@import "./assets/common.scss";
@import "./assets/variables.scss";

#hero {
  background-image: url("./assets/img/jumbotron.jpg");
  background-size: cover;
  height: 320px;
}

#currentSeriesComics {
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
