<template>
	<view class="index-list">
		<view class="index-list1">
			<view>
				<image :src="item.uerpic" mode="widthFix" lazy-load="" ></image>
				{{item.username}}
			</view>
			<view v-show="item.isguanzhu">
				<view class="icon iconfont icon-bofang"></view>关注
			</view>
		</view>
		<view class="index-list2">{{item.title}}</view>
		<view class="index-list3 common-center">
			<!--图片-->
			<image :src="item.titlepic" mode="widthFix" lazy-load></image>
			<template v-if="item.type=='video'">
				<view class="icon iconfont icon-bofang index-list-play" ></view>
				<view class="index-list-playinfo">
					{{item.playnum}}次播放 {{item.long}}
				</view>
			</template>
			
		</view>
		<view class="index-list4">
			<view>
				<view :class="{'active':(item.infonum.index==1)}"><view class="icon iconfont icon-bofang"></view>{{item.dingnum}}</view>
				<view><view class="icon iconfont icon-bofang"></view>{{item.cai}}</view>
			</view>
			<view>
				<view><view class="icon iconfont icon-bofang"></view>{{item.commentnum}}</view>
				<view><view class="icon iconfont icon-bofang"></view>{{item.sharenum}}</view>
			</view>
		</view>
	</view>
</template>

<script>
	export default {
		props:{
			item:Object,
			index:Number
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
		font-size: 24rpx;
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
		padding-top: 15upx;
		font-size: 32upx;
	}
	.common-center{
		justify-content: center;
		align-items: center;
	}
	.index-list3 {
		position: relative;
		border-radius: 20upx;
		justify-content: center;
		align-items: center;
	}
	.index-list-play {
		position: absolute;
		font-size: 50upx;
	}
	.index-list-playinfo {
		position: absolute;
		background-color: rgba(51,51,51,0.72);
		color: #FFFFFF;
		bottom: 8upx;
		right: 8upx;
		border-radius: 50upx;
		padding-left: 10upx;
		padding-right: 10upx;
	}
	.index-list4{
		display: flex;
		justify-content: space-between;
		align-content: center;
		padding: 15upx;
	}
	.index-list4>view{
		color: #999999;
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
	
	.index-list4>view>view>view{
		padding-right: 10upx;
	}
	
	.index-list4 .active,.index-list4 .active>view{
		color:#FF3333
	}
</style>
