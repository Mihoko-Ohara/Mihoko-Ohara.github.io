<template>
  <div>
    <!-- <toggle/> -->
      <h2 id="profile" class="box" v-scroll="handleScroll">PROFILE</h2>
        <profile/>
      <!-- <h2 id="about" class="box" v-scroll="handleScroll">ABOUT</h2> -->
        <!-- <about/> -->
      <h2 id="music" class="box" v-scroll="handleScroll">LIVE REPORT</h2>
        <music/>
      <h2 id="contact" class="box" v-scroll="handleScroll">CONTACT</h2>
        <contact/>
  </div>
</template>

<script>

import profile from '~/components/profile';
// import about from '~/components/about';
import music from '~/components/music';
import contact from '~/components/contact';
// import toggle from '~/components/toggle';

export default {
  components:{
    profile,
    // about,
    music,
    contact,
    // toggle
  },
    methods: {
      handleScroll: function(evt, el) {
      let top = el.getBoundingClientRect().top;
      if (window.scrollY > top + window.pageYOffset - 800) {
        el.classList.add("isView");
        return true;
      }
      return false;
    }
  },
  // data: () => {
  //   return {isMenuActive: false}
  // },
  // methods: {
  //   toggleMenu () {
  //     this.isMenuActive = !this.isMenuActive
  //   }
  // }
}
</script>

<style lang="scss" scoped>
.box.isView{
  opacity: 1;
  transform: translate(0, 0);
}

.box {
  opacity: 0;
  transform : translate(0, 50px);
  transition : all 1500ms;
  font-weight: bold;
  font-size: 1.5em;
  padding-top: 50px;
  padding-bottom: 20px;
}

@media screen and (max-width: 480px) {

  #nav-toggle{
    position: fixed;
    top: 10px;
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
    height: 1px;
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

   #gloval-nav {
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

    #gloval-nav a {
      display: block;
      color: #000;
      text-decoration: none;
      padding: 10px 0;
      transition: color .6s ease;
    }

    #gloval-nav ul {
      list-style: none;
    }

    #gloval-nav li {
      opacity: 0;
      transform: translateX(200px);
      transition:  transform .6s ease, opacity .2s ease;
    }


  .open {
      overflow: hidden;
    }

  .open #gloval-nav {
      visibility: visible;
      opacity: 1;
    }

   .open #gloval-nav li {
      opacity: 1;
      transform: translateX(0);
      transition:  transform 1s ease, opacity .9s ease;
    }

}
</style>