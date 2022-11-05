<template>
	<view class="box animate__animated animate__zoomIn" v-if="visible">
		<view class="overlay" @click="close"></view>
		<view class="modal">
			<view class="top">功能B</view>
			<view class="func-area">
				<view class="func" v-for="(item,index) in list" :key="index">
				<view class="logo">
					<img src="@/static/bag.png" alt="">
				</view>
					<view class="name">{{item}}</view>
				</view>
			</view>

		</view>
	</view>
</template>

<script>
	export default {
		name: "functionB",
		props:['visible'],
		data() {
			return {
				list:['功能1','功能2','功能3','功能4','功能5','功能6','功能7','功能8','功能9']
			};
		},
		methods:{
			close(){
				this.$emit('update:visible',false)
			}
		},
		mounted(){
			console.log(this.visible);
		}
	}
</script>

<style lang="scss">
	.box {
	 animation-duration: 0.2s; 
		position: fixed;
		top: 50rpx;
		height: 100%;
		width: 100%;
		display: flex;
		justify-content: center;
		align-items: center;
	}
	.overlay{
		position: fixed;
		top: 0;
		background-color: transparent;
		height: 100%;
		width: 100%;
		z-index: 10;
	}
	.modal {
		z-index: 11;
		overflow: hidden;
		border-radius: 15rpx;
		width: 95%;
		background-color: #f1f1f1;
		.top {
			height: 80rpx;
			display: flex;
			justify-content: center;
			align-items: center;
			color: #88bb38;
			font-size: 35rpx;
			background-color: #282a3a;
		}
		.func-area {
			display: flex;
			flex-wrap: wrap;
			.func {
				margin: 15rpx 0;
				display: flex;
				flex-direction: column;
				align-items: center;
				width: 25%;
				.logo {
				
					height: 100rpx;
					width: 100rpx;
					img{
						height: 100%;
						width: 100%;
					}
				}
				.name{
					
				}
			
			}
		}
	}
</style>
