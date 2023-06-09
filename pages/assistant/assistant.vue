<template>
	<view>
		<view>我是助手页面</view>
		<tabbar :pagePath="'pages/assistant/assistant'"></tabbar>
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
