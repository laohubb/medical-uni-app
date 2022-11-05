<template>
	<view class="tabbar">
		<view class="item active">
			<view class="logo"><i class="iconfont icon-paper"></i></view>
			<view class="name">工作</view>
		</view>
		<view class="item">
			<view class="logo"><i class="iconfont icon-shenghuozhushou"></i></view>
			<view class="name">助手</view>
		</view>
		<view class="middle">
			<view class="circle">
				<img src="@/static/tabbar-icon/plus.png">
				</view>
		</view>
		<view class="item">
			<view class="logo">
				<i class="iconfont icon-plus hide"></i>
			
			</view>
			<view class="name">常用</view>
		</view>
		<view class="item">
			<view class="logo"><i class="iconfont icon-shujufenxi-baobeifenxi"></i></view>
			<view class="name">分析</view>
		</view>
		<view class="item">
			<view class="logo"><i class="iconfont icon-me"></i></view>
			<view class="name">我的</view>
		</view>


	</view>
</template>

<script>
	export default {
		name: "TabBar",
		data() {
			return {

			};
		}
	}
</script>

<style lang="scss">
	$bottom-padding:25rpx;
	.tabbar {
		background-color: white;
		position: fixed;
		width: 100%;
		bottom: 0;
		display: flex;
		padding-bottom: $bottom-padding;
		border-top: 1rpx solid #dedede;
		.item {
			display: flex;
			flex-direction: column;
			justify-content: center;
			align-items: center;
			width: 20%;
			padding: 10rpx 0;
			color: #8e8e8e;
			margin-top: -6rpx;
			&.active{
				color: #88aa41;
			}
			.logo {
				font-size: 100rpx;
				
				.iconfont{
					font-size: 40rpx;
				}
				.hide {
					visibility: hidden;
				}
			}
			.name {
				font-size: 20rpx;
				text-align: center;
			}


		}

		.middle {
			position: fixed;
			bottom: (40rpx+$bottom-padding);
			width: 100%;
			display: flex;
			justify-content: center;
			width:100%;
			.circle{
				background-color: white;
				display: flex;
				justify-content: center;
				align-items: center;
				border-top: 1rpx solid #dedede;
				width: 85rpx;
				height: 85rpx;
				border-radius: 50%;
				img{
					width: 80rpx;
					height: 80rpx;
					
				}
			}
			
			
		}
	}
</style>
