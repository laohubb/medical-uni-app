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
			<view>
				<view class="">logo</view>
				<view class="">功能1</view>
			</view>
			<view>
				<view class="">logo</view>
				<view class="">功能1</view>
			</view>
			<view>
				<view class="">logo</view>
				<view class="">功能1</view>
			</view>
			<view>
				<view class="">logo</view>
				<view class="">功能1</view>
			</view>
			<view>
				<view class="">logo</view>
				<view class="">功能1</view>
			</view>
		</view>

		<view class="function">
			<view class="block">功能a</view>
			<view class="block">功能a</view>
			<view class="block">功能a</view>
			<view class="block">功能a</view>
			<view class="block">功能a</view>
			<view class="block">功能a</view>
			<view class="block">功能a</view>
			<view class="block">功能a</view>
			<view class="block">功能a</view>
			<view class="block">功能a</view>
		</view>

	</view>
</template>

<script>
	export default {
		data() {
			return {
				swiperList: ['']
			};
		}
	}
</script>

<style lang="scss">
	view{
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

		>view {
			text-align: center;
			color: white;
			width: 20%;
			height: 100%;

		}
	}

	.function {
		margin-top: 10rpx;
		height: 550rpx;
		background-color: white;
		display: flex;
		flex-wrap: wrap;

		.block {
			height: (100%/3);
			width: 25%;
			background-color: white;
			border: 1rpx solid gray;
		}
	}
</style>
