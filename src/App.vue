<template>
  <div id="app">
    <Header/>

    <main>
      <div class="content">
        <div class="container">
          -main content here-
        </div>
      </div>

      <div class="buy_comics_banner">
        <div class="container">
          <ul>
            <li>
              <img src="./assets/img/buy-comics-digital-comics.png" alt="icon">
              <span>DIGITAL COMICS</span>
            </li>
            <li>
              <img src="./assets/img/buy-comics-digital-comics.png" alt="icon">
              <span>DIGITAL COMICS</span>
            </li>
            <li>
              <img src="./assets/img/buy-comics-digital-comics.png" alt="icon">
              <span>DIGITAL COMICS</span>
            </li>
            <li>
              <img src="./assets/img/buy-comics-digital-comics.png" alt="icon">
              <span>DIGITAL COMICS</span>
            </li>
            <li>
              <img src="./assets/img/buy-comics-digital-comics.png" alt="icon">
              <span>DIGITAL COMICS</span>
            </li>
          </ul>          
        </div>
      </div>
    </main>

    <Footer/>
  </div>
</template>


<script>
import Header from "@/components/Header.vue";
import Footer from "@/components/Footer.vue";

export default {
  name: 'App',
  components: {
    Header,
    Footer
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

.buy_comics_banner {
  background-color: $main_color;

  ul {
    list-style: none;
    display: flex;
    justify-content: space-around;

    li {
      display: flex;
      align-items: center;
      color: white;
      padding: 3rem 0;

      img {
        width: 40px;
        margin-right: .75rem;
      }
    }
  }
}
</style>
