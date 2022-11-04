<template>
	<view>
		<view class="top">
			<view class="hide">铃铛</view>
			<view class="">早上好!张三先生</view>
			<view class="">铃铛</view>
		</view>
		<swiper :indicator-dots="true" :autoplay="true" :interval="3000" :duration="1000" :circular="true">
			<swiper-item>
				<view class="swiper-item">

					<img src="../../static/swiper/2.jpeg" alt="" srcset="">

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
		<functionB v-if="false"></functionB>
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
				functionList: ['功能A', '功能B', '功能C', '功能D', '功能E', '功能F', '功能G', '功能H', '功能I', '功能J', '', '']
			};
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
	}

	swiper {
		height: 320rpx;

		.swiper-item {
			height: 100%;

			img {
				width: 100%;

			}
		}

	}

	.menu {
		height: 120rpx;
		background-color: #282a3a;
		display: flex;
		align-items: center;

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

			.icon {
				height: 90rpx;
			}

		}
	}
</style>
