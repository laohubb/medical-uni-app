<template>

	<view>
		<view class="top">
			<view class="ring hide">
				<view class="number">77</view>
				<view class="logo">
					<svg t="1667624298016" class="icon" viewBox="0 0 1024 1024" version="1.1" xmlns="http://www.w3.org/2000/svg" p-id="2018" width="128" height="128"><path d="M924.964959 660.871515h-40.82604l-9.568603-280.679022C874.570316 177.976016 717.326273 0 513.196075 0A370.304937 370.304937 0 0 0 142.572185 367.434356v293.437159H95.68603a95.68603 95.68603 0 0 0-95.68603 95.686031 95.68603 95.68603 0 0 0 95.68603 95.68603h243.680424v2.232674a169.364273 169.364273 0 0 0 339.0475 0v-2.232674H924.964959a95.68603 95.68603 0 0 0 95.68603-95.68603 95.68603 95.68603 0 0 0-95.68603-95.686031z m-310.660645 191.372061a105.573587 105.573587 0 0 1-211.466127 0v-2.232674h210.82822s0.637907 1.913721 0.637907 2.551627zM924.964959 787.177075H95.68603a31.895343 31.895343 0 1 1 0-63.790687h78.781498a31.895343 31.895343 0 0 0 31.895344-31.895343v-312.574365A314.169133 314.169133 0 0 1 446.534808 70.807662C647.475471 25.197321 810.779629 191.37206 810.779629 380.192493l9.568603 280.679022v31.895344a31.895343 31.895343 0 0 0 31.895344 31.895343H924.964959a31.895343 31.895343 0 1 1 0 63.790687z" fill="" p-id="2019"></path></svg>
				</view>
			</view>
			<view class="">早上好!张三先生</view>
			<view class="ring">
				<view class="number">77</view>
				<view class="logo">
					<svg t="1667624298016" class="icon" viewBox="0 0 1024 1024" version="1.1" xmlns="http://www.w3.org/2000/svg" p-id="2018" width="128" height="128"><path d="M924.964959 660.871515h-40.82604l-9.568603-280.679022C874.570316 177.976016 717.326273 0 513.196075 0A370.304937 370.304937 0 0 0 142.572185 367.434356v293.437159H95.68603a95.68603 95.68603 0 0 0-95.68603 95.686031 95.68603 95.68603 0 0 0 95.68603 95.68603h243.680424v2.232674a169.364273 169.364273 0 0 0 339.0475 0v-2.232674H924.964959a95.68603 95.68603 0 0 0 95.68603-95.68603 95.68603 95.68603 0 0 0-95.68603-95.686031z m-310.660645 191.372061a105.573587 105.573587 0 0 1-211.466127 0v-2.232674h210.82822s0.637907 1.913721 0.637907 2.551627zM924.964959 787.177075H95.68603a31.895343 31.895343 0 1 1 0-63.790687h78.781498a31.895343 31.895343 0 0 0 31.895344-31.895343v-312.574365A314.169133 314.169133 0 0 1 446.534808 70.807662C647.475471 25.197321 810.779629 191.37206 810.779629 380.192493l9.568603 280.679022v31.895344a31.895343 31.895343 0 0 0 31.895344 31.895343H924.964959a31.895343 31.895343 0 1 1 0 63.790687z" fill="" p-id="2019"></path></svg>
				</view>
			</view>
		</view>
		<swiper :indicator-dots="true" :autoplay="true" :interval="3000" :duration="1000" :circular="true">
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
					<svg t="1667579384507" class="icon" viewBox="0 0 1024 1024" version="1.1"
						xmlns="http://www.w3.org/2000/svg" p-id="1452" width="128" height="128">
						<path d="M782.5 449.8m-120.2 0a120.2 120.2 0 1 0 240.4 0 120.2 120.2 0 1 0-240.4 0Z"
							fill="#B0CED8" p-id="1453"></path>
						<path
							d="M751.9 612.6H137.2c-44.5 0-81-36.5-81-81V339.7c0-44.5 36.4-81 81-81h614.7c44.5 0 81 36.4 81 81v191.9c0 44.5-36.5 81-81 81z"
							fill="#B0CED8" p-id="1454"></path>
						<path d="M152.139 485.613l63.564-36.7 206.55 357.745-63.564 36.7z" fill="#B0CED8" p-id="1455">
						</path>
						<path d="M546.6 258.7v353.6l285.7 144.9V142.4z" fill="#1983CD" p-id="1456"></path>
					</svg>
				</view>
				<view class="name">{{item}}</view>
			</view>

		</view>

		<view class="function">
			<view class="block" @click="openFunc">
				<view class="logo">
					<svg t="1667578329799" class="icon" viewBox="0 0 1024 1024" version="1.1"
						xmlns="http://www.w3.org/2000/svg" p-id="883" width="128" height="128">
						<path
							d="M789.333333 234.666667h-10.666666V192a85.333333 85.333333 0 0 0-85.333334-85.333333h-362.666666a85.333333 85.333333 0 0 0-85.333334 85.333333v42.666667H234.666667a128 128 0 0 0-128 128v42.666666h810.666666v-42.666666a128 128 0 0 0-128-128zM309.333333 192c0-11.754667 9.578667-21.333333 21.333334-21.333333h362.666666c11.754667 0 21.333333 9.578667 21.333334 21.333333v42.666667h-405.333334V192zM106.666667 448v341.333333a128 128 0 0 0 128 128h554.666666a128 128 0 0 0 128-128V448H106.666667z m503.786666 264.213333h-68.928v68.928a29.525333 29.525333 0 1 1-59.072-0.021333v-68.928h-68.928a29.525333 29.525333 0 1 1 0.021334-59.072h68.928v-68.928a29.525333 29.525333 0 1 1 59.072 0.021333v68.928h68.928a29.525333 29.525333 0 1 1-0.021334 59.072z"
							fill="#0367FD" p-id="884"></path>
					</svg>
				</view>
				<view class="name">功能B</view>

			</view>

			<view class="block" v-for="(item,index) in functionList" :key="index">
				<view class="logo">
					<svg t="1667578329799" class="icon" viewBox="0 0 1024 1024" version="1.1"
						xmlns="http://www.w3.org/2000/svg" p-id="883" width="128" height="128">
						<path
							d="M789.333333 234.666667h-10.666666V192a85.333333 85.333333 0 0 0-85.333334-85.333333h-362.666666a85.333333 85.333333 0 0 0-85.333334 85.333333v42.666667H234.666667a128 128 0 0 0-128 128v42.666666h810.666666v-42.666666a128 128 0 0 0-128-128zM309.333333 192c0-11.754667 9.578667-21.333333 21.333334-21.333333h362.666666c11.754667 0 21.333333 9.578667 21.333334 21.333333v42.666667h-405.333334V192zM106.666667 448v341.333333a128 128 0 0 0 128 128h554.666666a128 128 0 0 0 128-128V448H106.666667z m503.786666 264.213333h-68.928v68.928a29.525333 29.525333 0 1 1-59.072-0.021333v-68.928h-68.928a29.525333 29.525333 0 1 1 0.021334-59.072h68.928v-68.928a29.525333 29.525333 0 1 1 59.072 0.021333v68.928h68.928a29.525333 29.525333 0 1 1-0.021334 59.072z"
							fill="#0367FD" p-id="884"></path>
					</svg>
				</view>
				<view class="name">{{item}}</view>

			</view>

		</view>
		<functionB v-bind:visible.sync="show"></functionB>
	</view>
</template>

<script>
	import functionB from "@/components/functionB.vue"
	export default {
		components: {
			functionB
		},
		data() {
			return {
				swiperList: [''],
				menuList: ['功能A', '功能B', '功能C', '功能D', '功能E'],
				functionList: ['功能A', '功能C', '功能D', '功能E', '功能F', '功能G', '功能H', '功能I', '功能J', '', ''],
				show:false
			};
		},
		methods:{
			openFunc(){
				this.show=true
			}
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
		height: 120rpx;
		font-size: 40rpx;
		background-color: #282a3a;
		
		.hide {
			visibility: hidden;
		}
		.ring{
		
			height: 100%;
			width: 100rpx;
			.number{
				display: flex;
				align-items: center;
				justify-content: center;
				position: fixed;
				right: 10rpx;
				top: 100rpx;
				height: 40rpx;
				width: 40rpx;
				font-size: 10rpx;
				color: white;
				background-color: red;
				border-radius: 50%;
							
			}
			.logo{
				height: 100%;
				display: flex;
				justify-content: center;
				align-items: center;
				.icon{
				fill: #88bb38;
					width: 60rpx;
				}
			}
			
		}
	}

	


	swiper {
		height: 320rpx;
		.swiper-item {
			height: 100%;
			img {
				width: 100%;
			}
		}
		/deep/ .uni-swiper-dots {
			margin-bottom: -20rpx;
			.uni-swiper-dot {
				border: 1rpx solid #93be3a;
				background-color: transparent;
			}
			.uni-swiper-dot-active {
				border: 1rpx solid #93be3a;
				background-color: #93be3a;
			}
		}
	}



	.menu {
		height: 120rpx;
		background-color: #282a3a;
		display: flex;
		align-items: center;
		margin-top: -1rpx;
		.box {
			text-align: center;
			color: white;
			width: 20%;
			height: 100%;
			display: flex;
			flex-direction: column;
			justify-content: center;
			align-items: center;

			.icon {
				height: 70rpx;
			}

			.name {
				margin-top: -20rpx;
				color: #9c9d9c;
				font-size: 20rpx;
			}
		}
	}

	.function {
		margin-top: 10rpx;
		height: 550rpx;
		background-color: white;
		display: flex;
		flex-wrap: wrap;

		$border: 2rpx solid #f5f5f5;

		.block {
			height: (100%/3);
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


			.icon {
				height: 90rpx;
			}

		}
	}
</style>
