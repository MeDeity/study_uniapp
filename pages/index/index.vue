<template>
	<view class="content">
		<!-- <image class="logo" src="/static/logo.png"></image>
		<view class="text-area">
			<text class="title">{{title}}</text>
		</view> -->
		
		<view class="index-list">
			<view class="index-list1">
				<view>
					<image src="../../static/mine_select.png" mode="widthFix" lazy-load="" ></image>
					昵称
				</view>
				<view>
					<view class="icon iconfont icon-bofang"></view>关注
				</view>
			</view>
			<view class="index-list2">我是标题</view>
			<view class="index-list3"></view>
				<image src="../../static/logo.png" mode="widthFix"></image>
			<view class="index-list4">
				<view>
					<view><view class="icon iconfont icon-bofang"></view>10</view>
					<view><view class="icon iconfont icon-bofang"></view>10</view>
				</view>
				<view>
					<view><view class="icon iconfont icon-bofang"></view>10</view>
					<view><view class="icon iconfont icon-bofang"></view>10</view>
				</view>
			</view>
		</view>
		<navigator url="../ceshi/ceshi">
			<view class="icon iconfont icon-bofang" style="color: #09BB07;">播放</view>
			
			
		</navigator>
		
	</view>
</template>

<script>
	export default {
		data() {
			return {
				
			}
		},
		onLoad() {
			
		},
		methods: {

		}
	}
</script>

<style>
	.content {
		display: flex;
		flex-direction: column;
		align-items: center;
		justify-content: center;
	}

	.logo {
		height: 200rpx;
		width: 200rpx;
		margin-top: 200rpx;
		margin-left: auto;
		margin-right: auto;
		margin-bottom: 50rpx;
	}

	.text-area {
		display: flex;
		justify-content: center;
	}

	.title {
		font-size: 36rpx;
		color: #8f8f94;
	}

	.index-list{
		padding: 20upx;
		border-bottom: 1upx solid #999999;
	}
	.index-list1{
		display: flex;
		justify-content: space-between;
		align-items: center;
	}
	.index-list1>view:first-child{
		align-items: center;
		color: #999999;
	}
	
	.index-list1>view:first-child image{
		width: 90upx;
		height: 90upx;
		border-radius: 100%;
		margin-right: 10upx;
		align-content: center;
		align-items: center;
	}
	.index-list1>view:first-child{
		display: flex;
		align-content: center;
	}
	.index-list1>view:last-child{
		display: flex;
		align-items: center;
		padding-left: 15upx;
		padding-right: 15upx;
	}
	.index-list1>view:last-child view{
		margin-right: 10upx;
	}
	
	.index-list1>view:last-child{
		background-color: #929292;
		border-radius: 5upx;
	}
	
	.index-list2{
		
	}
	.index-list3{
		width: 100%;
		border-radius: 20upx;
	}
	.index-list4{
		display: flex;
		justify-content: space-between;
		align-content: center;
		padding: 15upx;
	}
	.index-list4>view:first-child{
		display: flex;
		align-content: center;
	}
	.index-list4>view:last-child{
		display: flex;
		align-content: center;
	}
	.index-list4>view>view{
		display: flex;
		align-items: center;
		padding: 10upx;
	}
</style>
