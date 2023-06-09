<template>
	<view>
		<view>我是我的页面</view>
		<tabbar :pagePath="'pages/my/my'"></tabbar>
	</view>
</template>

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
