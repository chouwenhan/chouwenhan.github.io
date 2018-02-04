<template>
<div class="home" style="margin:0; padding:0">
    <el-carousel :interval="4000" type="" height="300px">
        <el-carousel-item v-for="item in banner">
            <img v-bind:src="item">
        </el-carousel-item>
    </el-carousel>
    <div class="box-flex box-top2 flex-direction-column">
        <div class="box-flex box-1" v-for="(item,index) in homearticle">
        	<div class="box-flex box-padding" v-if="index%2==0">
        		<div class="box-flex-img">
        			<img class="images-con" v-bind:src="homearticle[index].src">
        		</div>
        		<div class="box-flex-text">
        			<div class="images-text">{{item.text}}</div>
        		</div>
            </div>
            <div class="box-flex box-padding" v-else>
        		<div class="box-flex-text">
        			<div class="images-text">{{item.text}}</div>
        		</div>
        		<div class="box-flex-img">
        			<img class="images-con" v-bind:src="homearticle[index].src">
        		</div>
            </div>
        </div>
    </div>
    <div class="box-mywork box-top3 flex-direction-column">
    	<div class="mywork-content">My work</div>
    </div>
</div>
</template>
<script>
export default {
  name: 'component',
  data () {
    return {
      title: 'Componest',
      banner: [require('./../assets/ba1.png'),
               require('./../assets/ba2.png'),
               require('./../assets/ba3.png')
              ],
      homearticle: [{'src':require('./../assets/article1.png'),'text':"React Native 应用及组件分享"},
                    {'src':require('./../assets/article2.png'),'text':"Docker compose 应用及分享"},
                    {'src':require('./../assets/article3.png'),'text':"PHP 应用及分享"},
                    {'src':require('./../assets/article4.png'),'text':"資料庫 应用及分享"}]
    }
  }
}
</script>
<style >
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
.box-flex {
	position: relative;
    height: 88vw;
    width: 100%;
}
.box-1 {
	width: 100%;
	height: 20vw;
}
.box-padding {
	/*height: 10vw;*/
    margin: 2vw 10vw 0 10vw;
}
.images-con {
	max-height: 20vw;
}
.box-flex-img, .box-flex-text {
	width: 40vw;
	float: left;
	height: 20vw;
}
.images-text, .images-con {
	-webkit-transition: 1s;
	width: 40vw;
	height: 20vw;
	line-height: 20vw;
}
.images-con:hover {
    -webkit-transform: scale(1.1);
}
/*end home article*/
/*home work*/
.box-mywork {
	position: relative;
	width: 100%;
	height: 5vw;
	line-height:5vw;
}
.mywork-content {
	clear:both;
	position: relative;
	font-size: 3vw;
	line-height:3vw;
}


/*end home work*/
</style>
