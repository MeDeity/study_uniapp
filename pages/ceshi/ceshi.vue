<template>
	<view class="animated tada">
		<view class="view-box animated" hover-class="view-box-hover tada" hover-start-time="2000">第一个view</view>
		<text id="first" selectable="true" space="nbsp">这 是 文 本</text>
		<view class="box">
			<view>{{mydata}}</view>
			<view>{{mydata}}</view>
			<view>{{user.name}}</view>
		</view>
		<button type="primary" @tap="changeUserName('dcloud')">更换名称</button>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				mydata:"2333",
				user:{
					name:"uni-app"
				}
			}
		},
		methods: {
			changeUserName:function(name){
				this.user.name = name;
			}
		}
	}
</script>

<style>
	.view-box{
		width: 200upx;
		height: 200upx;
		background: #0077AA;
		color: #000000;
		margin: 10upx;
	}
	.view-box-hover {
		background: #990055;
	}
	
	view>text{
		background: #09BB07;
	}
	
	.box {
		background: #990055;
		color: #007AFF;
		width: 300upx;
		height: 300upx;
		border-radius: 100%;
		display: flex;
	}
</style>
