<template>
<div class="home" style="margin:0; padding:0">
    <el-carousel :interval="4000" height="300px">
        <el-carousel-item v-for="(item,index) in banner" :key="index">
            <img v-bind:src="item">
        </el-carousel-item>
    </el-carousel>
    <div class="box-article flex flex-direction-column">
        <div class="box-article-one flex flex-direction-row" v-for="(item,index) in homearticle" :key="index">
            <div class="box flex flex-direction-row margin-lr" v-if="index%2==0">
                <div class="box-article-img flex flex-direction-column">
                    <img class="images-con line-height-article transition" v-bind:src="homearticle[index].src">
                </div>
                <div class="box-article-text flex flex-direction-column">
                    <div class="images-text line-height-article">{{item.text}}</div>
                </div>
            </div>
            <div class="box flex flex-direction-row margin-lr" v-else>
                <div class="box-article-text flex flex-direction-column">
                    <div class="images-text line-height-article">{{item.text}}</div>
                </div>
                <div class="box-article-img flex flex-direction-column">
                    <img class="images-con line-height-article transition" v-bind:src="homearticle[index].src">
                </div>
            </div>
        </div>
    </div>
    <div class="box-mywork line-height-mywork flex flex-direction-column">
        <div class="mywork-font-size">My work</div>
    </div>
    <div class="box-mywork-image flex flex-center flex-direction-column">
        <div class="flex flex-center flex-direction-row">
            <div class="flex flex-2 flex-direction-column">
                <div class="flex flex-2 flex-direction-column">
                    <img class="width-10vw height-20vh" src="../assets/image_mountain.png">
                </div>
                <div class="flex flex-2 flex-direction-column">
                   <img class="width-10vw height-20vh" src="../assets/image_people.png">
                </div>
                <div class="flex flex-2 flex-direction-column">
                   <img class="width-10vw height-20vh" src="../assets/image_street.png">
                </div>
            </div>
            <div class="flex flex-4 flex-direction-column">
                <div class="flex flex-4">
                   <img class="width-20vw height-40vh" src="../assets/image_cat.png">
                </div>
                <div class="flex flex-2 flex-direction-row">
                    <div class="flex flex-1 flex-direction-column">
                       <img class="width-10vw height-20vh" src="../assets/image_sea.png">
                    </div>
                    <div class="flex flex-1 flex-direction-column" >
                        <img class="width-10vw height-20vh" src="../assets/image_mountain.png">
                    </div>
                </div>
            </div>
            <div class="flex flex-2 flex-direction-column">
                <div class="flex flex-2 flex-direction-column">
                    <img class="width-10vw height-20vh" src="../assets/image_people.png">
                </div>
                <div class="flex flex-2 flex-direction-column">
                    <img class="width-10vw height-20vh" src="../assets/image_street.png">
                </div>
                <div class="flex flex-2 flex-direction-column">
                    <img class="width-10vw height-20vh" src="../assets/image_doll.png">
                </div>
            </div>
        </div>
    </div>
    <div class="box-my-skill flex flex-direction-column" style="margin-top:8vh;background-color: #69cb89;">
        <div class="box-my-skill-text-box flex flex-center flex-direction-row" style="margin-bottom:2vh">
            <div class="font-size-6vh margin-tb">My Skill</div>
        </div>
        <div class="box-my-skill-circle-box flex flex-center flex-direction-row">
           <div class="flex flex-direction-column margin-lr-1vw">
                <el-progress type="circle" :percentage="60"></el-progress>
                <span>JavaScript</span>
            </div>
            <div class="flex flex-direction-column margin-lr-1vw">
                <el-progress type="circle" :percentage="80"></el-progress>
                <span>PHP</span>
            </div>
            <div class="flex flex-direction-column margin-lr-1vw">
                <el-progress type="circle" :percentage="60"></el-progress>
                <span>Mysql</span>
            </div>
            <div class="flex flex-direction-column margin-lr-1vw">
                <el-progress type="circle" :percentage="50"></el-progress>
                <span>Vue</span>
            </div>
        </div>
    </div>
    <div class="box-my-person-profile flex flex-direction-column yellow-color">
        <div class="flex flex-1 flex-center">
            <div class="my-person-profile-text">Personal Profile</div>
        </div>
        <div class="flex flex-4 flex-center flex-direction-row">
            <div class="flex flex-1 flex-direction-column margin-left-15vw">
                <div class="flex flex-1 flex-direction-row margin-tb-1vh">
                    <div class="flex flex-1 "> <Icon class="icon" type="person" size="30"></Icon> </div>
                    <div class="flex flex-4 text-align-left" style="font-size:20px;">hank</div>
                </div>
                <div class="flex flex-1 flex-direction-row margin-tb-1vh">
                    <div class="flex flex-1 "> <Icon class="icon" type="ios-email" size="30"></Icon> </div>
                    <div class="flex flex-4 text-align-left" style="font-size:20px;">a29554483@gmail.com </div>
                </div>
                <div class="flex flex-1 flex-direction-row margin-tb-1vh">
                    <div class="flex flex-1 "> <Icon class="icon" type="ios-telephone" size="30"></Icon> </div>
                    <div class="flex flex-4 text-align-left" style="font-size:20px;">0987539752</div>
                </div>
                <div class="flex flex-5 flex-direction-row margin-tb-1vh ">
                    <div class="flex flex-1 "> <Icon class="icon-book" type="ios-paper" size="30"></Icon> </div>
                    <div class="flex flex-4 text-align-left">
                            <p>年齡: 27歲
                            <br>目前居住地: 台北
                            <br>任職: 宏碁
                            <br>職稱: 程式設計師
                            <br>技能： web前端: vue,bootstrap,js,jquery
                            <br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; web後端: php,slim,mysql
                            <br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; 環境相關: docker,linux,git
                            <br>GitHub個人主頁面： https://chouwenhan.github.io/dist/index.html#/home
                            </p>
                    </div>
                </div>
            </div>
            <div class="flex flex-1 flex-direction-column " >
                <div class="box-my-person-profile-img margin-auto">
                    <img class="radius" style="width:100%;height:100%" src="../assets/profile.png">
                </div>
            </div>
        </div>
    </div>
    <div class="box-mylink-box flex flex-center flex-direction-column">
        <div class="flex flex-1 flex-center" style="color: #999;">© 2018 All rights reserved. Design and development by Hank Chou</div>
        <div class="flex flex-1 flex-center" style="color: #999;">Projects made with</div>
        <mylink></mylink>
        <div class="flex flex-2 flex-center flex-direction-row">
            <!-- Start of CuterCounter Code -->
            <div class ="flex flex-1 flex-center" style="font-size:2vh;margin-right:0.5vw;color: white">訪客人數:
            </div>
            <div class ="flex flex-1 flex-center" >
                <div href="http://www.cutercounter.com/traditional-chinese/" target="_blank"><img src="http://www.cutercounter.com/hit.php?id=9536&nd=6&style=50" border="0" alt="免费計數器"></div>
                <!-- End of CuterCounter Code -->
            </div>
        </div>
    </div>
</div>
</template>
<script>
import mylink from './mylink.vue'
export default {
  name: 'Home',
  data () {
    return {
      title: 'Componest',
      banner: [require('./../assets/ba1.png'),
        require('./../assets/ba2.png'),
        require('./../assets/ba3.png')
      ],
      homearticle: [{'src': require('./../assets/article1.png'), 'text': 'React Native 应用及组件分享'},
        {'src': require('./../assets/article2.png'), 'text': 'Docker compose 应用及分享'},
        {'src': require('./../assets/article3.png'), 'text': 'PHP 应用及分享'},
        {'src': require('./../assets/article4.png'), 'text': '資料庫 应用及分享'}]
    }
  },
  components: {
    mylink
  }
}
</script>
<style >
@media screen and (min-width: 768px){
    /*common use*/
    .yellow-color {
        background-color: #FFFFE0;
    }
    .flex-direction-row {
        flex-direction: row;
    }
    .flex-direction-column {
        flex-direction: column;
    }
    .flex {
        display: -webkit-flex;
    }
    .flex-center {
        -webkit-align-items: center;
        -webkit-justify-content: center;
    }
    .flex-6 {
        flex: 6;
    }
    .flex-4 {
        flex: 4;
    }
    .flex-2 {
        flex: 2;
    }
    .flex-1 {
        flex: 1;
    }
    .flex-start {
        align-items:flex-start;
        justify-content:flex-start;
    }
    .left {
        float: left;
    }
    .width-10vw {
        max-width: 10vw;
    }
    .width-20vw {
        max-width: 20vw;
    }
    .height-20vh {
        height: 20vh;
    }
    .height-40vh {
        height: 40vh;
    }
    /*********************************************************/
    .home {
        width: 100%;
        height: auto;
        overflow: hidden;
    }
    .el-carousel__item img {
        color: #475669;
        font-size: 14px;
        opacity: 0.75;
        line-height: 500px;
        margin: 0;
    }
    .el-carousel__item:nth-child(2n) {
        background-color: #99a9bf;
    }
    .el-carousel__item:nth-child(2n+1) {
        background-color: #d3dce6;
    }
    /*home article*/
    .box {
        width: auto;
        height: auto;
    }
    .box-article {
        height: 80vw;
        width: 100%;
    }
    .box-article-one {
        width: 100%;
        height: 20vw;
    }
    .margin-auto {
        margin: auto;
    }
    .margin-lr {
        margin: 0vw auto;
    }
    .margin-tb {
        margin: auto 0vw;
    }
    .margin-tb-1vh {
        margin: 1vh 0vw;
    }
    .margin-lr-1vw {
        margin: 0vw 1vw;
    }
    .margin-left-15vw {
        margin-left: 15vw;
    }
    .images-con {
        max-height: 20vw;
    }
    .box-article-img, .box-article-text {
        width: 40vw;
        height: 20vw;
    }
    .transition {
        -webkit-transition: 1s;
    }
    .line-height-article {
        line-height: 20vw;
    }
    .images-text, .images-con {
        width: 40vw;
        height: 20vw;
    }
    .images-con:hover {
        -webkit-transform: scale(1.1);
    }
    /*end home article*/
    /*my work*/
    .line-height-mywork {
        line-height:5vw;
    }
    .box-mywork {
        width: 100%;
        height: 5vw;
    }
    .mywork-font-size {
        font-size: 3vw;
    }
    /*end my work*/
    /*my work imagebox*/
    .box-mywork-image {
        height: 60vh;
    }
    .myimage-row {
        display: -webkit-flex;
        flex-direction: row;
    }
    .myimage-column {
        flex-direction: column;
        flex: 2;
    }
    /*my work end*/
    /*home myskill*/

    .box-my-skill {
        height: 40vh;
        width: 100%;
    }
    .box-my-skill-text-box {
        height:10vh;
        width: 100%;
    }
    .font-size-6vh {
       font-size: 6vh;
    }
    .box-my-skill-circle-box {
        height: 28vh;
        width: 100%;
    }
    /*home myskill end*/
    /*home person profile*/
    .box-my-person-profile {
        height: 60vh;
        width: 100%;
    }
    .box-my-person-profile-text-box {
        height:10vh;
        width: 100%;
    }
    .my-person-profile-text {
        display: -webkit-flex;
        align-items: center;
        justify-content: center;
        font-size: 3vw;
        line-height:3vw;
        color: black;
    }
    .my-person-profile-content-box {
        display: -webkit-flex;
        height:50vh;
        width: 100%;
        flex-direction: row;
    }
    .text-align-left {
        text-align: left;
    }
    .icon {
        margin: auto;
    }
    .icon-book {
        margin: 0 auto;
    }
    .box-my-person-profile-img {
        height: 20vh;
        width: 10vw;
    }
    .radius {
        border-radius: 200px;
    }
    /*home person profile end*/
    /*home mylink*/
    .box-mylink-box {
        background-color: #333;
        width: 100%;
        height: 16vh;
    }
}
/*************************************************************/

@media screen and (max-width: 768px){
    /*common use*/
    .box-my-person-profile .flex-5,.box-my-person-profile .flex-5 .flex-4  {
        margin-left: 6vw !important;
    }
    .yellow-color {
        background-color: #FFFFE0;
    }
    .flex-direction-row {
        flex-direction: row;
    }
    .flex-direction-column {
        flex-direction: column;
    }
    .flex {
        display: -webkit-flex;
    }
    .flex-warp {
        flex-wrap:wrap;
    }
    .flex-center {
        -webkit-align-items: center;
        -webkit-justify-content: center;
    }
    .flex-6 {
        flex: 6;
    }
    .flex-4 {
        flex: 4;
    }
    .flex-2 {
        flex: 2;
    }
    .flex-1 {
        flex: 1;
    }
    .flex-start {
        align-items:flex-start;
        justify-content:flex-start;
    }
    .left {
        float: left;
    }
    .width-10vw {
        width: 10vw;
    }
    .width-20vw {
        width: 20vw;
    }
    .height-20vh {
        height: 20vh;
    }
    .height-40vh {
        height: 40vh;
    }
    /*********************************************************/
    .home {
        width: 100%;
        height: auto;
        overflow: hidden;
    }
    .el-carousel__item img {
        color: #475669;
        font-size: 14px;
        opacity: 0.75;
        line-height: 500px;
        margin: 0;
    }
    .el-carousel__item:nth-child(2n) {
        background-color: #99a9bf;
    }
    .el-carousel__item:nth-child(2n+1) {
        background-color: #d3dce6;
    }
    /*home article*/
    .box {
        width: auto;
        height: auto;
    }
    .box-article {
        height: 80vw;
        width: 100%;
    }
    .box-article-one {
        width: 100%;
        height: 20vw;
    }
    /*.margin-auto {
        margin: auto;
    }*/
    .margin-lr {
        margin: 0vw auto;
    }
    .margin-tb {
        margin: auto 0vw;
    }
    .margin-tb-1vh {
        margin: 1vh 0vw;
    }
    .margin-lr-1vw {
        margin: 0vw 1vw;
    }
    .margin-left-15vw {
        margin-left: 0vw;
    }
    .images-con {
        max-height: 20vw;
    }
    .box-article-img, .box-article-text {
        width: 40vw;
        height: 20vw;
    }
    .transition {
        -webkit-transition: 1s;
    }
    .line-height-article {
        line-height: 20vw;
    }
    .images-text, .images-con {
        width: 40vw;
        height: 20vw;
    }
    .images-con:hover {
        -webkit-transform: scale(1.1);
    }
    /*end home article*/
    /*my work*/
    .line-height-mywork {
        line-height:5vw;
    }
    .box-mywork {
        width: 100%;
        height: 5vw;
    }
    .mywork-font-size {
        font-size: 3vw;
    }
    /*end my work*/
    /*my work imagebox*/
    .box-mywork-image {
        width: 100%;
        overflow: hidden;
        height: 60vh;
    }
    .myimage-row {
        display: -webkit-flex;
        flex-direction: row;
    }
    .myimage-column {
        flex-direction: column;
        flex: 2;
    }
    /*my work end*/
    /*home myskill*/

    .box-my-skill {
        height: 40vh;
        width: 100%;
    }
    .box-my-skill-text-box {
        height: 10vh;
        width: 100%;
    }
    .font-size-6vh {
       font-size: 6vh;
    }
    .el-progress-circle {
        height: 20vw !important;
        width: 20vw !important;
    }
    .box-my-skill-circle-box {
        height: 28vh;
        width: 100%;
    }
    /*home myskill end*/
    /*home person profile*/
    .box-my-person-profile {
        height: 60vh;
        width: 100%;
    }
    .box-my-person-profile-text-box {
        height:10vh;
        width: 100%;
    }
    .my-person-profile-text {
        display: -webkit-flex;
        align-items: center;
        justify-content: center;
        font-size: 3vw;
        line-height:3vw;
        color: black;
    }
    .my-person-profile-content-box {
        display: -webkit-flex;
        height:50vh;
        width: 100%;
        flex-direction: row;
    }
    .text-align-left {
        text-align: left;
    }
    .icon {
        margin: auto;
    }
    .icon-book {
        margin: 0 auto;
    }
    .box-my-person-profile-img {
        height: 10vh;
        width: 10vw;
    }
    .radius {
        border-radius: 200px;
    }
    /*home person profile end*/
    /*home mylink*/
    .box-mylink-box {
        background-color: #333;
        width: 100%;
        height: 16vh;
    }
}
</style>
