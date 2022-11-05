<template>
	<view class="box" v-if="visible">
		<view class="overlay" @click="close"></view>
		<view class="modal">
			<view class="top">功能B</view>
			<view class="func-area">
				<view class="func" v-for="(item,index) in list" :key="index">
					<view class="logo">
						<svg t="1667578329799" class="icon" viewBox="0 0 1024 1024" version="1.1" xmlns="http://www.w3.org/2000/svg" p-id="883" width="128" height="128"><path d="M789.333333 234.666667h-10.666666V192a85.333333 85.333333 0 0 0-85.333334-85.333333h-362.666666a85.333333 85.333333 0 0 0-85.333334 85.333333v42.666667H234.666667a128 128 0 0 0-128 128v42.666666h810.666666v-42.666666a128 128 0 0 0-128-128zM309.333333 192c0-11.754667 9.578667-21.333333 21.333334-21.333333h362.666666c11.754667 0 21.333333 9.578667 21.333334 21.333333v42.666667h-405.333334V192zM106.666667 448v341.333333a128 128 0 0 0 128 128h554.666666a128 128 0 0 0 128-128V448H106.666667z m503.786666 264.213333h-68.928v68.928a29.525333 29.525333 0 1 1-59.072-0.021333v-68.928h-68.928a29.525333 29.525333 0 1 1 0.021334-59.072h68.928v-68.928a29.525333 29.525333 0 1 1 59.072 0.021333v68.928h68.928a29.525333 29.525333 0 1 1-0.021334 59.072z" fill="#0367FD" p-id="884"></path></svg>
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
	
	 animation-duration: 0.5s; 

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
				.icon{
					height: 90rpx;
				}
				.name{
					margin-top: -10rpx;
				}
				display: flex;
				flex-direction: column;
				align-items: center;
				width: 25%;
				
			
			}
		}
	}
</style>
