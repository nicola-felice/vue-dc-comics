<template>
  
  <footer>

    <div class="footer_top">
      <div class="container">
        <div>
          <nav class="footer_nav">
            <ul>
              <h3>DC COMICS</h3>
              <li><a href="#">characters</a></li>
              <li><a href="#">comics</a></li>
              <li><a href="#">movies</a></li>
              <li><a href="#">TV</a></li>
              <li><a href="#">games</a></li>
              <li><a href="#">videos</a></li>
            </ul>
          </nav>
          <nav class="footer_nav">
            <ul>
              <h3>SHOP</h3>
              <li><a href="#">shop DC</a></li>
              <li><a href="#">shop DC collectibles</a></li>
            </ul>
          </nav>
        </div>

        <nav class="footer_nav">
          <ul>
            <h3>DC</h3>
            <li><a href="#">terms of use</a></li>
            <li><a href="#">privacy policy</a></li>
            <li><a href="#">ad choices</a></li>
            <li><a href="#">advertising</a></li>
            <li><a href="#">jobs</a></li>
            <li><a href="#">subscriptions</a></li>
            <li><a href="#">talent workshops</a></li>
            <li><a href="#">certificates</a></li>
            <li><a href="#">ratings</a></li>
            <li><a href="#">shop help</a></li>
            <li><a href="#">contact us</a></li>
          </ul>
        </nav>

        <nav class="footer_nav">
          <ul>
            <h3>SITES</h3>
            <li><a href="#">DC</a></li>
            <li><a href="#">MAD magazine</a></li>
            <li><a href="#">DC univerce</a></li>
            <li><a href="#">DC kids</a></li>
            <li><a href="#">DC power visa</a></li>
          </ul>
        </nav>      

        <img class="logo_footer_bg" src="../assets/img/dc-logo-bg.png" alt="">
      </div>
    </div>

    <div class="footer_bottom"></div>
  </footer>

</template>


<script>
export default {
  name: 'Footer'
}
</script>


<style scoped lang="scss">

.footer_top {
  background-color: black;
  overflow: hidden;
  background-image: url("../assets/img/footer-bg.jpg");

  .container {
    display: flex;
    padding: 2rem 0;
    position: relative;
  }

  .footer_nav {

    h3 {
      color: white;
    }

    ul {
      list-style: none;
      padding: .5rem;
      margin-right: .5rem;

      h3 {
        margin-bottom: .35rem;
      }

      li {
        text-transform: capitalize;
        font-size: .9rem;
        margin: .15rem;
      }
    }

    a {
      color: #959595;
      text-decoration: none;
      
    }
  }

  .logo_footer_bg {
    position: absolute;
    height: 130%;
    right: 0;
    top: 50%;
    transform: translateY(-50%);
  }
}
</style>