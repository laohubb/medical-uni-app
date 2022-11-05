<template>

	<view>
		<view class="top">
			<view class="ring hide">
				<view class="number">77</view>
				<view class="logo">
				</view>
			</view>
			<view class="">早上好!张三先生</view>
			<view class="ring">
				<view class="logo">
					<img src="@/static/ring.png" alt="">
				</view>
				<view class="number">77</view>

			</view>
		</view>
		<swiper :indicator-dots="true" :autoplay="true" :interval="3000" :duration="1000" :circular="true"
			indicator-color="rgba(255, 255, 255, 0.6)" indicator-active-color="#9dbd50">
			<swiper-item>
				<view class="swiper-item">
					<img src="../../static/swiper/2.jpeg" alt="" srcset="">
				</view>
			</swiper-item>
			<swiper-item>
				<view class="swiper-item">
					<img src="../../static/swiper/1.jpeg" alt="" srcset="">
				</view>
			</swiper-item>
		</swiper>

		<view class="menu">
			<view class="box" v-for="(item,index) in menuList" :key="index">
				<view class="logo">
					<img src="@/static/trumpet.png" alt="">
				</view>
				<view class="name">{{item}}</view>
			</view>

		</view>

		<view class="function">
			<view class="block" @click="openFunc">
				<view class="logo">
					<img src="@/static/bag.png" alt="">

				</view>

				<view class="name">功能B</view>

			</view>

			<view class="block" v-for="(item,index) in functionList" :key="index">
				<view class="logo">

					<img src="@/static/bag.png" alt="">
				</view>
				<view class="name">{{item}}</view>

			</view>

		</view>

		<FunctionB v-bind:visible.sync="show"></FunctionB>


		<TabBar></Tabbar>
	</view>
</template>

<script>
	import FunctionB from "@/components/FunctionB.vue"
	import TabBar from "@/components/TabBar.vue"
	export default {
		components: {
			FunctionB,
			TabBar
		},
		data() {
			return {
				swiperList: [''],
				menuList: ['功能A', '功能B', '功能C', '功能D', '功能E'],
				functionList: ['功能A', '功能C', '功能D', '功能E', '功能F', '功能G', '功能H', '功能I', '功能J', '', ''],
				show: false
			};
		},
		methods: {
			openFunc() {
				this.show = true
			}
		},
		options: {
			styleIsolation: 'shared'
		}

	}
</script>

<style lang="scss">
	view {
		box-sizing: border-box;
	}

	.top {
		display: flex;
		justify-content: space-between;
		align-items: center;
		color: #88bb38;
		height: 100rpx;
		font-size: 36rpx;
		background-color: #282a3a;

		.hide {
			visibility: hidden;
		}

		.ring {
			height: 100%;
			width: 100rpx;

			display: flex;
			align-items: center;
			justify-content: center;

			.logo {
				width: 60rpx;
				height: 60rpx;

				img {
					width: 100%;
					height: 100%;
				}
			}

			.number {
				position: fixed;
				display: flex;
				align-items: center;
				justify-content: center;
				right: 10rpx;
				top: 10rpx;
				height: 40rpx;
				width: 40rpx;
				font-size: 10rpx;
				color: white;
				background-color: red;
				border-radius: 50%;
				font-size: 20rpx;
			}


		}
	}




	swiper {
		height: 320rpx;

		.swiper-item {
			height: 100%;
			width: 100%;

			img {
				width: 100%;
				height: 100%;
			}
		}

	}



	.menu {
		height: 120rpx;
		background-color: #282a3a;
		display: flex;
		align-items: center;
		margin-top: -10rpx;

		.box {
			text-align: center;
			color: white;
			width: 20%;
			height: 100%;
			display: flex;
			flex-direction: column;
			justify-content: center;
			align-items: center;

			.logo {
				margin-top: 10rpx;
				height: 52rpx;
				width: 52rpx;

				img {
					height: 100%;
					width: 100%;
				}
			}

			.name {

				color: #9c9d9c;
				font-size: 20rpx;
			}
		}
	}

	.function {
		margin-top: 10rpx;
	
		background-color: white;
		display: flex;
		flex-wrap: wrap;
		$border: 2rpx solid #f5f5f5;

		.block {
		
			padding: 30rpx;
			width: 25%;
			background-color: white;
			border: $border;
			display: flex;
			flex-direction: column;
			justify-content: center;
			align-items: center;

			& {
				border-right: none;
				border-bottom: none;
			}

			&:nth-child(4n+1) {
				border-left: none;
			}

			&:nth-child(9),
			&:nth-child(10),
			&:nth-child(11),
			&:nth-child(12) {
				border-bottom: $border;
			}

			;

			&:nth-child(11),
			&:nth-child(12) {
				.logo {
					display: none;
				}

			}

			.logo {
				height: 100rpx;
				width: 100rpx;

				img {
					height: 100%;
					width: 100%;
				}
			}

			.name {
				font-size: 20rpx;
			}

		}
	}
</style>
