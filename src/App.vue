<template>
  <div id="app">

    <Header/>

    <main>
      <HeroSection :bg-src="require('./assets/img/jumbotron.jpg')" />

      <ComicsSeries/>

      <BuyComicsBanner/>
    </main>

    <Footer/>

  </div>
</template>


<script>
// components
import Header from "./components/Header.vue";
import Footer from "./components/Footer.vue";
import ComicsSeries from "./components/ComicsSeries.vue";
import BuyComicsBanner from "./components/BuyComicsBanner.vue";
import HeroSection from "./components/HeroSection.vue";

export default {
  name: 'App',
  components: {
    Header,
    Footer,
    BuyComicsBanner,
    HeroSection,
    ComicsSeries
  }, 
}
</script>


<style lang="scss">
@import "./assets/common.scss";
@import "./assets/variables.scss";

</style>
