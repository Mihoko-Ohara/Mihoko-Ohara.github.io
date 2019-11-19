<template>

        <div class="top-menu">
            <div id="top-btn" class="header-logo">
                <img src="~/assets/images/M_logo.png">
            </div>
            <div class="header-menu">
                <ul>
                    <li><nuxt-link v-scroll-to="'#profile'" to>PROFILE</nuxt-link></li>
                    <li><nuxt-link v-scroll-to="'#about'" to>ABOUT</nuxt-link></li>
                    <li><nuxt-link v-scroll-to="'#music'" to>LIVE REPORT</nuxt-link></li>
                    <li><nuxt-link v-scroll-to="'#contact'" to>CONTACT</nuxt-link></li>
                </ul>
            </div>
        </div>

</template>

<style lang="scss" scoped>
.top-menu{
  display: flex;
  height: 60px;
  position: -webkit-sticky;
  position: sticky;
  top: 0;
  z-index: 10;
}

.header-menu{
    a{
        position: relative;
        display: inline-block;
    }
}

.header-menu{
    a{
        &::after{
            position: absolute;
            bottom: 10px;
            left: 0;
            content: '';
            width: 100%;
            height: 1px;
            background: #333;
            transform: scale(0, 1);
            transform-origin: left top;
            transition: transform .3s;
        }
    }
}

.header-menu {
    a{
        &:hover{
            &::after{
                transform: scale(1, 1);
            }
        }
    }
}

.header-menu{
    ul{
       display: flex;
       line-height: 60px;
    }
}

.header-menu{
    li{
        padding-left: 20px;
        list-style: none;
    }
}

.header-logo{
    img{
        width: 50px;
        height: 50px;
        padding-top: 5px;
        padding-left: 15px;
    }
}

@media screen and (max-width: 480px){
  #top-btn img{
    width: 30px;
    height: 30px;
    padding-left: 5px;
  }

  .header-menu{
    display: none;
  }

}

</style>