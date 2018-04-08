<template>
	<div class="fixedheader width-100 zindex-100 height-120 text-align-center ">
        <div class="width-80 margin-auto box-flex text-align-center flex-direction-row flex-wrap flex-justify-center flex-items-center height-100">
	        <div class="flex-1 height-30 text-align-left flex-self-center ">
	            <span class="ion-navicon-round font-size-26" @click="openBottomSheet"></span>
	        </div>
	        <div class="flex-3 height-30 height-50 line-height-50 flex-direction-row flex-items-flex-start unselect">
	            <div class="flex-2"><img class="height-60" src="../assets/logo_b.png" lazy="loaded"></div>
	        </div>
	        <div class="flex-1 height-30 text-align-right flex-self-center">
	          <router-link to="/surch">
	          <span class="ion-search font-size-26"></span>
	          </router-link>
	        </div>
        </div>
    </div>
</template>
<script>
export default {
  name: 'teheader'
}
</script>
<style>
.fixedheader {
	width: 100%;
	height: 60px; /* 視情況而定(本例依圖片高度而設定) */
	position: fixed;
	top:0px;
	z-index: 9999;
	background-color: #FFAA33;
}
.height-60 {
	height: 60px;
}
</style>