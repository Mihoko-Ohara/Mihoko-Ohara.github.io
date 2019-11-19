// <template>
//     <div id="about-history" class="about-wrapper">
//         <div id="aboutlist">
//             <ul>
//             <li v-for="list in lists" :key='list'>{{list.writing}}</li>
//             <li>2019年 大学でバイオインフォマティクスという分野で蝶の擬態について研究中
//             <br>使用言語はPerl。それと同時にhtml、CSS、jQueryなどを勉強中。</li>
//             </ul>
//         </div>
//     </div>
// </template>

// <script>
// export default {
//     data: function() {
//         return {
//             lists: [
//                 {writing: '1995年 鹿児島で生まれる'},
//                 {writing: '2014年 鹿児島県立鶴丸高等学校を卒業'},
//                 {writing: '2015年 九州工業大学に入学、プログラミング(主にC言語)を学び始める'},
//                 {writing: '2018年 Life is Tech!の研修でWeb制作を経験し、Webに興味を持ち始める'}
//             ]
//         }
//     }
// }
// </script>

// <style lang="scss" scoped>
// .about-wrapper li{
//   list-style: square;
//   margin-left: 30em;
//   line-height: 2.8em;
// }

// @media screen and (max-width: 1200px) {
//   #about-history li{
//     margin-left: 180px;
//   }
// }

// @media screen and (max-width: 480px){
//     #about-history li{
//         margin-left: 20px;
//     }
// }

// </style>