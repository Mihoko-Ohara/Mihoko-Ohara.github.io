<template>
    <div class="contact-wrapper">
            <p>Follow me!</p>
        <ul id="sns">
            <li v-for="circle in circles" :key='circle'>
                <a class="circle" target="_blank" rel="noopener" v-bind:href="circle.href">
                    <i v-bind:class="circle.class"></i>
                </a>
            </li>
        </ul>
     </div>
</template>

<script>
export default {
    data: function() {
        return {
            circles: [
            {
                href: 'https://twitter.com/mihoko_ohara',
                class: 'fab fa-twitter'
            },
            {
                href: 'https://www.instagram.com/butterfly_mihoko',
                class: 'fab fa-instagram'
            },
            {
                href: 'https://www.facebook.com/mihoko.ohara.376',
                class: 'fab fa-facebook-f'
            }
            ]
        }
  }
}
</script>

<style lang="scss" scoped>
.contact-wrapper{
  margin-bottom: 20px;
}

.contact-wrapper p{
  text-align: center;
}

.contact-wrapper li{
  display: inline;
  padding-left: 10px;
  padding-right: 10px;
}

.contact-wrapper ul{
  padding-top: 15px;
  text-align: center;
}

.fab{
  font-size: 20px;
  line-height: 40px;
}

.circle{
  color: white;
  display: inline-block;
  width: 40px;
  height: 40px;
  border-radius: 50%;
  background: #000000;
  text-align:center;
  line-height: 40px;
  box-shadow:4px 4px 4px 2px #696969;
}

.circle:hover{
  background-color: #696969;
}
</style>