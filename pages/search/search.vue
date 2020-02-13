<template>
	<view>
		搜索
	</view>
</template>

<script>
	export default {
		data() {
			return {
				
			}
		},
		onNavigationBarButtonTap(e) {
			if(e.index==0){
				uni.navigateBack({
					delta:1,
					animationDuration:1000
				})
			}
		},
		methods: {
			
		}
	}
</script>

<style>

</style>
