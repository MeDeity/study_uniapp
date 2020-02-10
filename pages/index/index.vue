<template>
	<view>
		<block v-for="(item,index) in list" :key="index">
			<index-list :item="item" :index="index"></index-list>
		</block>
	</view>
</template>

<script>
	import indexList from "../../components/index/index-list.vue"
	
	export default {
		components:{
			indexList
		},
		data() {
			return {
				list:[
					{
						uerpic:"../../static/logo.png",
						username:"昵称",
						isguanzhu:false,
						title:"我是标题",
						type:"img",
						titlepic:"../../static/logo.png",
						playnum:20,
						long:'2:47',
						infonum:{
							index:0,//0 未操作 1 顶 2 踩
							dingnum:11,
							cai:11
						},
						commentnum:11,
						sharenum:10
					},
					{
						uerpic:"../../static/logo.png",
						username:"昵称",
						isguanzhu:false,
						title:"我是标题",
						type:"img",
						titlepic:"../../static/logo.png",
						playnum:20,
						long:'2:47',
						infonum:{
							index:0,//0 未操作 1 顶 2 踩
							dingnum:11,
							cai:11
						},
						commentnum:11,
						sharenum:10
					}
				]
			};
		}
	}
</script>

<style>

</style>
