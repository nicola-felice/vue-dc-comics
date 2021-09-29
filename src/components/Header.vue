<template>

  <header>
    <div class="container">
      <div class="logo_wrapper">
        <img class="logo" src="../assets/img/dc-logo.png" alt="DC logo">
      </div>

      <nav class="header_nav">
        <ul>
          <li><a href="#">comics</a></li>
          <li><a class="active" href="#">comics</a></li>
          <li><a href="#">comics</a></li>
          <li><a href="#">comics</a></li>
          <li><a href="#">comics</a></li>
          <li><a href="#">comics</a></li>
        </ul>
      </nav>      
    </div>
  </header>

</template>


<script>
export default {
  name: 'Header',
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
    padding: 2.5rem 0;
    margin-left: 2rem;
    text-transform: uppercase;
    font-weight: bold;
    letter-spacing: .35px;

    &.active {
      border-bottom: 5px $main_color solid;
      color: $main_color;
    }
  }
}  
</style>
