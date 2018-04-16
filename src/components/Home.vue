<template>
<div class="home" style="margin:0; padding:0">
    <el-carousel :interval="4000" type="" height="300px">
        <el-carousel-item v-for="item in banner">
            <img v-bind:src="item">
        </el-carousel-item>
    </el-carousel>
    <div class="box-flex box-top2 flex-direction-column">
        <div class="box-flex box-1" v-for="(item,index) in homearticle">
        	<div class="box-1 box-padding" v-if="index%2==0">
        		<div class="box-flex-img">
        			<img class="images-con" v-bind:src="homearticle[index].src">
        		</div>
        		<div class="box-flex-text">
        			<div class="images-text">{{item.text}}</div>
        		</div>
            </div>
            <div class="box-1 box-padding" v-else>
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
    <div class="box-myimage box-top4 flex-direction-column">
    	<div class="myimage-row" style="height:60vh">
    		<div class="myimage-column">
    			<div style="height:20vh">
    				<img class="images-height100" src="../assets/image_mountain.png">
    			</div>
    			<div style="height:20vh">
    				<img class="images-height100" src="../assets/image_people.png">
    			</div>
    			<div style="height:20vh">
    				<img class="images-height100" src="../assets/image_street.png">
    			</div>
    		</div>
            <div class="myimage-column flex-4">
    			<div class="flex-4" style="height:40vh">
    				<img class="images-height100" src="../assets/image_cat.png">
    			</div>
    			<div class="flex flex-2 flex-direction-row" style="height:20vh;">
	    			<div class="flex-1" style="width:50%;height:20vh;">
	    				<img class="images-height100" src="../assets/image_sea.png">
	    			</div>
	    			<div class="flex-1" style="width:50%;height:20vh;">
	    				<img class="images-height100" src="../assets/image_mountain.png">
	    			</div>
	    		</div>
    		</div>
    		<div class="myimage-column">
    			<div style="height:20vh">
    				<img class="images-height100" src="../assets/image_people.png">
    			</div>
    			<div style="height:20vh">
    				<img class="images-height100" src="../assets/image_street.png">
    			</div>
    			<div style="height:20vh">
    				<img class="images-height100" src="../assets/image_doll.png">
    			</div>
    		</div>
    	</div>
    </div>
    <div class="my-skill">
    	<div class="my-skill-text-box">
    		<div class="my-skill-text">My Skill</div>
    	</div>
    	<div class="my-skill-circle-box">
	    	<div class="flex-direction-column">
				<el-progress type="circle" class="margin-right-1" :percentage="60"></el-progress>
	            <span>JavaScript</span>
	        </div>
			<div class="flex-direction-column">
				<el-progress type="circle" class="margin-right-1" :percentage="80"></el-progress>
				<span>PHP</span>
			</div>
			<div class="flex-direction-column">
				<el-progress type="circle" class="margin-right-1" :percentage="60"></el-progress>
				<span>Mysql</span>
			</div>
	        <div class="flex-direction-column">
				<el-progress type="circle" class="margin-right-1" :percentage="50"></el-progress>
				<span>Vue</span>
			</div>
		</div>
    </div>
    <div class="my-person-profile">
    	<div class="my-person-profile-text-box">
    		<div class="my-person-profile-text">Personal Profile</div>
    	</div>
    	<div class="my-person-profile-content-box">
    		<div class="my-person-profile-content-text-box">
    			<div class="flex flex-direction-row ">	</div>
    				<div class="flex flex-1">	</div>
    				<div class="flex flex-2">	</div>
    			<div class="flex flex-direction-row ">	</div>
    				<div class="flex flex-1">	</div>
    				<div class="flex flex-4">	</div>
    			<div class="flex flex-direction-row ">	</div>
    				<div class="flex flex-1">	</div>
    				<div class="flex flex-4">	</div>
    			<div class="flex flex-direction-row ">	</div>
    		</div>
    		<div class="my-person-profile-photo-box">	
    		</div>
    	</div>
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
    margin: 2vw 10vw 0vw 10vw;
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
/*home imagebox*/
.box-myimage {
	width: 100%;
	display: -webkit-flex;
	-webkit-align-items: center;
	-webkit-justify-content: center;
}
.myimage-row {
	display: -webkit-flex;
	flex-direction: row;
}
.myimage-column {
	flex-direction: column;
	flex: 2;
}
.images-height100 {
	height: 100%;
}
.flex {
	display: -webkit-flex;
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
.flex-direction-row {
	flex-direction: row;
}
.flex-start {
	align-items:flex-start;
	justify-content:flex-start;
}
/*home work end*/
/*home myskill*/
.my-skill {
	display: -webkit-flex;
	flex-direction: column;
	height: 40vh;
	width: 100%;
	background-color: #69cb89;
	margin-top:8vh; 
}
.my-skill-text-box {
	display: -webkit-flex;
	align-items: center;
	justify-content: center;
	height:10vh;
	width: 100%;
	margin-bottom: 2%; 
}
.my-skill-text {
	display: -webkit-flex;
	align-items: center;
	justify-content: center;
	font-size: 3vw;
	line-height:3vw;
    color: white;
}
.my-skill-circle-box {
	display: -webkit-flex;
	flex-direction: row;
	align-items: center;
	justify-content: center;
}
.flex-direction-column {
	flex-direction: column;
}
.margin-right-1 {
	margin-right: 1%; 
}
/*home myskill end*/
.my-person-profile {
	display: -webkit-flex;
	flex-direction: column;
	height: 60vh;
	width: 100%;
}
.my-person-profile-text-box {
	display: -webkit-flex;
	align-items: center;
	justify-content: center;
	height:20vh;
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
	height:40vh;
	width: 100%;
	align-items:flex-start;
	justify-content:flex-start;
	flex-direction: row;
}
.my-person-profile-content-text-box {
	display: -webkit-flex;
	width: 50%;
	flex-direction: column;
	align-items: center;
	justify-content: center;
}
/*home person profile*/
</style>
