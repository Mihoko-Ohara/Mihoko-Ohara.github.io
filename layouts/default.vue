<template>
  <div :class="{'open': isMenuActive}">
  <div>
    <div id="nav-toggle" data-target="navMenu" @click="toggleMenu">
      <div>
        <span></span>
        <span></span>
        <span></span>
      </div>
    </div>
    <div id="navMenu" class="responsive-menu">
        <ul>
          <li @click="toggleMenu"><img src="~/assets/images/M_logo.png" width="35px" height="35px"></li>
          <!-- <li><a id="menu1" href="#profile">PROFILE</a></li>
          <li><a id="menu2" href="#about">ABOUT</a></li>
          <li><a id="menu3" href="#music">MUSIC</a></li>
          <li><a id="menu4" href="#contact">CONTACT</a></li> -->
          <li @click="toggleMenu"><nuxt-link v-scroll-to="'#profile'" to>PROFILE</nuxt-link></li>
          <!-- <li @click="toggleMenu"><nuxt-link v-scroll-to="'#about'" to>ABOUT</nuxt-link></li> -->
          <li @click="toggleMenu"><nuxt-link v-scroll-to="'#music'" to>LIVE REPORT</nuxt-link></li>
          <li @click="toggleMenu"><nuxt-link v-scroll-to="'#contact'" to>CONTACT</nuxt-link></li>
          <li @click="toggleMenu">
            <a target="_blank" rel="noopener" href="https://twitter.com/mihoko_ohara">
              <i class="fab fa-twitter"></i>
            </a>
          </li>
          <li @click="toggleMenu">
            <a target="_blank" rel="noopener" href="https://www.instagram.com/butterfly_mihoko">
              <i class="fab fa-instagram"></i>
            </a>
          </li>
          <li @click="toggleMenu">
            <a target="_blank" rel="noopener" href="https://www.facebook.com/mihoko.ohara.376">
              <i class="fab fa-facebook-f"></i>
            </a>
          </li>
        </ul>
    </div>
</div>

    <Name/>
    <TheHeader/>
    <main class="contents">
      <nuxt/>
    </main>
    <TheFooter/>
  </div>
</template>

<script>
import TheHeader from '~/components/TheHeader';
import TheFooter from '~/components/TheFooter';
import Name from '~/components/Name';

export default {
  components:{
    TheHeader,
    TheFooter,
    Name
  },
    data: () => {
    return {isMenuActive: false}
  },
  methods: {
    toggleMenu () {
      this.isMenuActive = !this.isMenuActive
    }
  }
}

</script>

<style lang="scss" scoped>

@media screen and (max-width: 480px) {

  #nav-toggle{
    position: fixed;
    top: 23px;
    right: 15px;
    height: 32px;
    z-index: 1000;
    }

  #nav-toggle div{
    position: relative;
    width: 36px;
  }

  #nav-toggle span{
    width: 100%;
    height: 1.2px;
    left: 0;
    display: block;
    background: #333;
    position: absolute;
    transition: transform .6s ease-in-out, top .5s ease;
  }

  #nav-toggle span:nth-child(1){
      top: 0;
    }
  #nav-toggle span:nth-child(2){
      top: 10px;
    }
  #nav-toggle span:nth-child(3){
      top: 20px;
    }

   .open #nav-toggle span {
      background: #000;
     }

    .open #nav-toggle span:nth-child(1) {
       top: 15px;
       transform: rotate(45deg);
     }
    .open #nav-toggle span:nth-child(2) {
        top: 15px;
        width: 0;
        left: 50%;
      }
    .open #nav-toggle span:nth-child(3) {
        top: 15px;
        transform: rotate(-45deg);
      }

    .main-wrapper{
     z-index: 900;
    }

   .responsive-menu {
      background: rgba(245, 245, 245, 0.8);
      color: #000;
      position: fixed;
      top: 0;
      left: 0;
      right: 0;
      bottom: 0;
      z-index: 990;
      text-align: center;
      display: flex;
      visibility: hidden;
      flex-direction: column;
      justify-content: center;
      align-items: center;
      font-size: 29px;
      opacity: 0;
      transition: opacity .6s ease, visibility .6s ease;
  }

    .responsive-menu{
      a {
      display: block;
      color: #000;
      text-decoration: none;
      padding: 10px 0;
      transition: color .6s ease;
      }
    }

    .responsive-menu{
      ul {
      list-style: none;
    }
    }

    .responsive-menu{
      li {
      opacity: 0;
      transform: translateX(200px);
      transition:  transform .6s ease, opacity .2s ease;
    }
    }


  .open {
      overflow: hidden;
    }

  .open{
    .responsive-menu {
      visibility: visible;
      opacity: 1;
    }
  }

   .open{
     .responsive-menu{
       li {
      opacity: 1;
      transform: translateX(0);
      transition:  transform 1s ease, opacity .9s ease;
      }
    }
   }
}
</style>