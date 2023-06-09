<template>
	<view>
		<view>我是分析页面</view>
		<tabbar :pagePath="'pages/analysis/analysis'"></tabbar>
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
