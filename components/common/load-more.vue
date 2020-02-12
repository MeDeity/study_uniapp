<template>
	<!--上拉加载-->
	<view class="loading-more">{{loadText}}</view>
</template>

<script>
	export default {
		props:{
			loadText:String
		},
		methods: {
			
		}
	}
</script>

<style scoped>
    .loading-more {
        align-items: center;
        justify-content: center;
        padding-top: 10px;
        padding-bottom: 10px;
        text-align: center;
    }
</style>
