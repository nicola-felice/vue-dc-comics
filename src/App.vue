<template>
  <div id="app">
    
    <Header/>

    <main>
      <div class="content">
        <div class="container">
          -main content here-
        </div>
      </div>

      <BuyComicsBanner/>
    </main>

    <Footer/>

  </div>
</template>


<script>
import Header from "@/components/Header.vue";
import Footer from "@/components/Footer.vue";
import BuyComicsBanner from "@/components/BuyComicsBanner.vue";

export default {
  name: 'App',
  components: {
    Header,
    Footer,
    BuyComicsBanner
  }
}
</script>


<style lang="scss">
@import "@/assets/common.scss";
@import "@/assets/variables.scss";

.content {
  background-color: black;
  padding: 3rem;
  color: white;
  font-size: 2rem;
}
</style>
