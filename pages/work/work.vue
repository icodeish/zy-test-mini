<template>
	<view class="container" style="position: relative;">
		<div class="title">
			<text>早上好!  张三先生</text>
			<view class="msg">
				<msg></msg>
			</view>
		</div>
		<view class="swiper">
			<swiper indicator-active-color="green" :indicator-dots="true" :autoplay="true" :interval="3000" :duration="1000">
				<swiper-item>
					<img style="width:100%;" src="../../static/tabbar/banner.png" alt="">
				</swiper-item>
				<swiper-item>
					<img style="width:100%;" src="../../static/tabbar/banner.png" alt="">
				</swiper-item>
				<swiper-item>
					<img style="width:100%;" src="../../static/tabbar/banner.png" alt="">
				</swiper-item>
				<swiper-item>
					<img style="width:100%;" src="../../static/tabbar/banner.png" alt="">
				</swiper-item>
			</swiper>
		</view>
		<view class="menu">
			<view class="item_menu" v-for="item in menuList">
				<view>
					<img class="img" :src="item.path" alt="">
				</view>
				<view class="">
					<text>{{item.name}}</text>
				</view>
			</view>
		</view>
		<view class="card">
			<view @click="toGongnengb(item.name)" class="item_card" v-for="item in cardList">
				<view >
					<img :src="item.path" alt="">
				</view>
				<view class="">
					<text>{{item.name}}</text>
				</view>
			</view>
		</view>
		<view @click="hidePop()" v-if="show" class="mask">
			
		</view>
		<view v-if="show" class="pop">
				<view class="pop_title">
					功能B
				</view>
				<view class="card1">
				<view  class="item_card1" v-for="item in cardList">
					<view >
						<img :src="item.path" alt="">
					</view>
					<view class="">
						<text>{{item.name}}</text>
					</view>
				</view>
				</view>
		</view>
		<tabbar :pagePath="'pages/work/work'"></tabbar>
	</view>
	
</template>  

<script>
	export default {
		data(){
			return{
				show:false,
				menuList:[
					
					{
						id:0,
						name:'功能1',
						path:'../../static/menu/rili.png'
					},
					{
						id:1,
						name:'功能2',
						path:'../../static/menu/dh.png'
					},
					{
						id:2,
						name:'功能3',
						path:'../../static/menu/rili.png'
					},
					{
						id:3, 
						name:'功能4',
						path:'../../static/menu/dh.png'
					},
					{
						id:4,
						name:'功能5',
						path:'../../static/menu/rili.png'
					}
				],
				
				cardList:[
					{
						id:0,
						name:'功能A',
						path:'../../static/menu/yl.png'
					},
					{
						id:1,
						name:'功能B',
						path:'../../static/menu/yy.png'
					},
					{
						id:2,
						name:'功能C',
						path:'../../static/menu/yl.png'
					},
					{
						id:3,
						name:'功能D',
						path:'../../static/menu/yy.png'
					},
					{
						id:4,
						name:'功能E',
						path:'../../static/menu/yl.png'
					},
					{
						id:5,
						name:'功能F',
						path:'../../static/menu/yy.png'
					},
					{
						id:6,
						name:'功能G',
						path:'../../static/menu/yl.png'
					},
					{
						id:7,
						name:'功能H',
						path:'../../static/menu/yy.png'
					},
					{
						id:8,
						name:'功能I',
						path:'../../static/menu/yl.png'
					},
					{
						id:9,
						name:'功能J',
						path:'../../static/menu/yy.png'
					}
				],
			}
		},
		methods:{
			toGongnengb(val){
			if(val==='功能B'){
				this.show=true
			}
			},
			hidePop(){
				this.show=false
			}
		}
	};
</script>

<style lang="scss">
	page{
		background-color: #999;
	}
	.title{
		width: 100%;
		height: 60px;
		background-color: #000;
		display: flex;
		justify-content: center;
		align-items: center;
	}
	.title text{
		color: green;
		font-size: 20px;
	}
	.msg{
		position:absolute;
		right: 20px;
	}
	.menu{
		width: 100%;
		height: 100px;
		background-color: #000;
		color:#999;
		display: flex;
		justify-content: space-around;
		align-items: center;
	}
	
	.item_menu{
		text-align: center;
	}
	.card{
		display: flex;
		flex-wrap: wrap;
		background-color: #fff;
		
		
	}
	.item_card{
		width: 25%;
		text-align: center;
		box-sizing: border-box;
		border-right:1px solid #999;
		border-bottom:1px solid #999;
		padding: 10px  0;
	}
	.card1{
		display: flex;
		flex-wrap: wrap;
		background-color: #fff;
	
		margin: 0 auto;
		
		
	}
	.item_card1{
		width: 25%;
		text-align: center;
		box-sizing: border-box;
		padding: 10px  0;
	}
	.item_card1 img{
		width:80px;
		height: 80px;
		
	}
	.item_card img{
		width:80px;
		height: 80px;
		
	}
	.mask{
		position: fixed;
		top: 0;
		left:0;
		opacity: 0.8;
		background-color:#000;
		height: 100%;
		width: 100%;
		
	}
	.pop_title{
		margin: 0 auto;
		text-align: center;
		height: 40px;
		border-top-right-radius: 5px ;
		border-top-left-radius: 5px ;
		background-color: #000;
		color: green;
		line-height: 40px;
		font-size: 20px;
	}
	.pop{
		width: 90%;
		position: fixed;
		top:50%;
		left: 50%;
		transform: translate(-50%,-50%);
	}
	.img{
		width:40px;
		height:40px;
	}
</style>
