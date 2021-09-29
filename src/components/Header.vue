<template>

  <header>
    <div class="container">
      <div class="logo_wrapper">
        <a href="#"><img class="logo" src="../assets/img/dc-logo.png" alt="DC logo"></a>
      </div>

      <nav class="header_nav">
        <ul>
          <li v-for="(elm, index) in menu" :key="index"><a :class="{ 'active' : elm.isActive }" :href="elm.link">{{elm.name}}</a></li>
        </ul>
      </nav>      
    </div>
  </header>

</template>


<script>
export default {
  name: 'Header',
  data() {
    return {
      menu: [
        {
          link: '#',
          name: 'characters',
          isActive: false,
        },
        {
          link: '#',
          name: 'comics',
          isActive: true,
        },
        {
          link: '#',
          name: 'movies',
          isActive: false,
        },
        {
          link: '#',
          name: 'TV',
          isActive: false,
        },
        {
          link: '#',
          name: 'games',
          isActive: false,
        },
        {
          link: '#',
          name: 'collectibles',
          isActive: false,
        },
        {
          link: '#',
          name: 'videos',
          isActive: false,
        },
        {
          link: '#',
          name: 'fans',
          isActive: false,
        },
        {
          link: '#',
          name: 'news',
          isActive: false,
        },
        {
          link: '#',
          name: 'shop',
          isActive: false,
        },
      ]
    }
  }
}
</script>


<style scoped lang="scss">
@import "@/assets/variables.scss";

.container {
  display: flex;
  justify-content: space-between;
  align-items: center;
}

.logo {
  width: 70px;
}

.header_nav ul {
  display: flex;
  list-style: none;

  a {
    color: black;
    text-decoration: none;
    display: block;
    padding: 2.5rem .85rem;
    text-transform: uppercase;
    letter-spacing: .45px;
    font-weight: bold;

    &.active {
      border-bottom: 5px $main_color solid;
      color: $main_color;
    }

    &:hover {
      border-bottom: 5px $main_color solid;
    }
  }
}  
</style>
