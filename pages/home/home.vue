<template>
	<view>
		<swiper :indicator-dots="true" :autoplay="true" :interval="3000" :duration="1000" :circular="true">
			<swiper-item>
				<view class="swiper-item">
				
					<img src="../../static/swiper/2.jpeg" alt="" srcset="">

				</view>
			</swiper-item>

		</swiper>
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
	swiper {
		height: 320rpx;
		
		.swiper-item {
			height: 100%;
		
			img {
				width: 100%;
		
			}
		}

	}
</style>
