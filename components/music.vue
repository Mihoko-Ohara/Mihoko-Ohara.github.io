<template>
    <div class="music-wrapper">
        <div id="musicexplain">
            <div v-for="item in items" :key='item' class="liveReport">
                <img :src="item.photo" class="liveImage">
                <p class="live-title">{{item.title}}</p>
                <p>{{item.day}}</p>
            </div>
        </div>
    </div>
</template>

<script>
import Image1 from '~/assets/images/liveReport/IMG_0266.jpg';
import Image2 from '~/assets/images/liveReport/IMG_0263.jpg';
import Image3 from '~/assets/images/liveReport/IMG_0265.jpg';
import Image4 from '~/assets/images/liveReport/IMG_0308.jpg';
import Image5 from '~/assets/images/liveReport/IMG_0267.jpg';
import Image6 from '~/assets/images/liveReport/IMG_4413.jpg';
import Image7 from '~/assets/images/liveReport/IMG_5208.jpg';
import Image8 from '~/assets/images/liveReport/IMG_0268.jpg';
export default {
    data: function() {
        return {
            items: [
                {photo: Image1, title: "WILD BUNCH FEST 2015", day: "Yamaguchi Aug 23"},
                {photo: Image2, title: "WILD BUNCH FEST 2016", day: "Yamaguchi Aug 20,21"},
                {photo: Image3, title: "WILD BUNCH FEST 2017", day: "Yamaguchi Aug 19,20"},
                {photo: Image4, title: "TRIANGLE 2017", day: "Fukuoka Aug 26"},
                {photo: Image5, title: "COUNT DOWN JAPAN 1718", day: "Tokyo Dec 30,31-Jan 1"},
                {photo: Image6, title: "TRIANGLE 2018", day: "Fukuoka Aug 25,26"},
                {photo: Image7, title: "BARIYOKA ROCK 2018", day: "Fukuoka Dec 26"},
                {photo: Image8, title: "SUMMER SONIC 2019", day: "Osaka Aug 16"}
            ]
        }
  }
}
</script>

<style lang="scss" scoped>
.music-wrapper{
  text-align: center;
}


.liveReport{
    display: inline-block;
    color: #708090;
}

.live-title{
    font-weight: bold;
    margin-bottom: 4px;
}

.liveImage{
    width: 280px;
    height: 250px;
    margin-left: 50px;
    margin-right: 50px;
    margin-bottom: 10px;
    padding-top: 20px;
}
</style>