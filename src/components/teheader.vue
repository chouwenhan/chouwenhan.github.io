<template>
	<div class="fixedheader">
        <div>
	        <div>
	            <span class="ion-navicon-round font-size-26" @click="openBottomSheet"></span>
	        </div>
	        <div >
	            <div class="flex-2"><img class="height-60" src="../assets/logo_b.png" lazy="loaded"></div>
	        </div>
	        <div >
	          <router-link to="/surch">
	          <span></span>
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