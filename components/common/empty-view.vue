<template>
	<view class="empty content-center animated fadeInUp">
		<image src="../../static/bg_empty.jpg" mode="widthFix"></image>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				
			}
		},
		methods: {
			
		}
	}
</script>

<style scoped>
	.empty{
		
		position: absolute;
		top: 0;
		bottom: 0;
		left: 0;
		right: 0;
	}
	.empty image {
		width: 60%;
	}
	
	.content-center{
		justify-content: center;
		align-items: center;
	}
</style>
