<template>
<div class="profile-wrapper">
        <img src="~/assets/images/IMG_9737.JPG">
        <p class="profile-name">大原 美穂子</p>
    <div id="explain">
        <p v-for="sentence in sentences" :key= 'sentence'>{{sentence.writing}}</p>
    </div>
</div>
</template>

<script>
export default {
  data: function() {
    return {
    sentences: [
        {writing: '1995年、鹿児島生まれ。'},
        {writing: '鹿児島県立鶴丸高等学校を卒業後、'},
        {writing: '九州工業大学生命情報工学科に入学。'},
        {writing: '現在は大学の研究室でバイオインフォマティクス'},
        {writing: 'という分野を学ぶとともに'},
        {writing: 'Web開発に興味を持ち勉強中。'},
        {writing: '九工大MusicサークルAgeha 主催。'}
      ]
    }
  }
}
</script>

<style lang="scss" scoped>
.profile-wrapper img{
  width: 250px;
  height: 250px;
  display: block;
  margin: auto;
}

.profile-name{
  text-align: center;
  padding-top: 10px;
  padding-bottom: 10px;
}

.profile-wrapper p{
  text-align: center;
  line-height: 2em;
}

.profile-wrapper br{
  line-height: initial;
}

</style>