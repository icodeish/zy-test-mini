<template>
	<view class="container">
		<view>我是常用页面</view>
		<tabbar :pagePath="'pages/main/main'"></tabbar>
	</view>
</template>
<style>
	
</style>
<script> 
	export default {
		data() {
			return {
				
			}
		},
		onLoad() {
			uni.hideTabBar();
		},
		methods: {
			
		}
	}
</script>

<style>
