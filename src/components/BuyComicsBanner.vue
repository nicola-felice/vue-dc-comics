<template>
  <div class="buy_comics_banner">
    <div class="container">
      <ul>
        <li v-for="(elm, index) in links" :key="index">
          <a :href="elm.link">
            <img :src="elm.src" alt="icon">
            <span>{{elm.name}}</span>              
          </a>
        </li>
      </ul>          
    </div>
  </div>
</template>


<script>
export default {
  name: 'BuyComicsBanner',
  data() {
    return {
      links: [
        {
          src: require('../assets/img/buy-comics-digital-comics.png'),
          link: '#',
          name: 'DIGITAL COMICS'
        },
        {
          src: require('../assets/img/buy-comics-merchandise.png'),
          link: '#',
          name: 'DC MERCHANDISE'
        },
        {
          src: require('../assets/img/buy-comics-subscriptions.png'),
          link: '#',
          name: 'SUBSCRIPTION'
        },
        {
          src: require('../assets/img/buy-comics-shop-locator.png'),
          link: '#',
          name: 'COMIC SHOP LOCATOR'
        },
        {
          src: require('../assets/img/buy-dc-power-visa.svg'),
          link: '#',
          name: 'DC POWER VISA'
        },
      ]
    }
  }
}
</script>


<style lang="scss" scoped>
@import "../assets/variables.scss";

.buy_comics_banner {
  background-color: $main_color;

  ul {
    list-style: none;
    display: flex;
    justify-content: space-around;

    li a {
      display: flex;
      align-items: center;
      color: white;
      text-decoration: none;
      margin: 3rem 0;

      img {
        height: 45px;
        margin-right: .75rem;
      }
    }
  }
}
</style>>
