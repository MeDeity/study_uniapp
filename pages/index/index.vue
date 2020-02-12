<template>
	<view class="uni-tab-bar">
		<swiper-tab-header :tabBars="tabBars" :tabIndex="tabIndex" @tabtap="ontabtap"></swiper-tab-header>
		
		<swiper :indicator-dots="false" :autoplay="false" class="swiper-box" 
		:style="{height:swiperHeight+'px'}" 
		:current="tabIndex"
		@change="tabChange">
			<swiper-item v-for="(items,index) in newsList" :key="index">
				<scroll-view scroll-y="true" class="scroll-v list">
					<block v-for="(item,id) in items" :key="id">
						<!-- <block v-for="(data,id1) in item" :key="id1"> -->
							<index-list :item="item" :index="id"></index-list>
						<!-- </block> -->
					</block>
				</scroll-view>
			</swiper-item>
		</swiper>
		<!-- <view class="uni-tab-bar">
			<scroll-view scroll-x="true" class="uni-tab-bar">
				<block v-for="item in tabBars" :key="item.id">
					<view class="swiper-tab-list">
						{{item.name}}
					</view>
				</block>
			</scroll-view>
		</view> -->
		
		<!-- <block v-for="(item,index) in list" :key="index">
			<index-list :item="item" :index="index"></index-list>
		</block> -->
	</view>
</template>

<script>
	import indexList from "../../components/index/index-list.vue";
	import swiperTabHeader from "../../components/index/swiper-tab-header.vue";
	export default {
		components:{
			indexList,
			swiperTabHeader
		},
		methods:{
			ontabtap(index) {
				this.tabIndex = index
			    // let index = e.target.dataset.current || e.currentTarget.dataset.current;
			    // this.switchTab(index);
				
			},
			tabChange(e) {
				console.log(JSON.stringify(e.detail));
				this.tabIndex = e.detail.current;
			}
		},
		onLoad() {
			uni.getSystemInfo({
				success: (res) =>{
					let height = res.windowHeight -uni.upx2px(100);
					this.swiperHeight = height;
				}
			})
		},
		data() {
			return {
				tabBars: [
				{
				    name: '关注',
				    id: 'guanzhu'
				}, {
				    name: '推荐',
				    id: 'tuijian'
				}, {
				    name: '体育',
				    id: 'tiyu'
				}, {
				    name: '热点',
				    id: 'redian'
				}, {
				    name: '财经',
				    id: 'caijing'
				}, {
				    name: '娱乐',
				    id: 'yule'
				}, {
				    name: '军事',
				    id: 'junshi'
				}, {
				    name: '历史',
				    id: 'lishi'
				}, {
				    name: '本地',
				    id: 'bendi'
				}],
				scrollInto: "",
				showTips: false,
				navigateFlag: false,
				pulling: false,
				tabIndex: 0,
				swiperHeight:500,
				newsList: [[
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
						],					
						[
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
						],				

						[
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
						],
						[
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
						],				

						[
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
						],				

						[
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
						],				

						[
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
						],				

						[
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
						],				

						[
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
						]
					
				],
			};
		}
	}
</script>

<style>
	.swiper-box {
	    flex: 1;
		height: 700upx;
	}
.tabs {
        flex: 1;
        flex-direction: column;
        overflow: hidden;
        background-color: #ffffff;
        /* #ifdef MP-ALIPAY || MP-BAIDU */
        height: 100vh;
        /* #endif */
    }

    .scroll-h {
        width: 750upx;
        height: 80upx;
        flex-direction: row;
        /* #ifndef APP-PLUS */
        white-space: nowrap;
        /* #endif */
        /* flex-wrap: nowrap; */
        /* border-color: #cccccc;
		border-bottom-style: solid;
		border-bottom-width: 1px; */
    }

    .line-h {
        height: 1upx;
        background-color: #cccccc;
    }

    .uni-tab-item {
        /* #ifndef APP-PLUS */
        display: inline-block;
        /* #endif */
        flex-wrap: nowrap;
        padding-left: 34upx;
        padding-right: 34upx;
    }

    .uni-tab-item-title {
        color: #555;
        font-size: 30upx;
        height: 80upx;
        line-height: 80upx;
        flex-wrap: nowrap;
        /* #ifndef APP-PLUS */
        white-space: nowrap;
        /* #endif */
    }

    .uni-tab-item-title-active {
        color: #FF3434;
    }

	.uni-tab-item-title-active .swiper-tab-list{
		border-bottom: 6upx solid;
		color: #FEDE33;
		width: 60upx;
		margin: auto;
		border-top: 6upx solid #FEDE33;
		border-radius: 20upx;
	}
    .swiper-box {
        flex: 1;
    }

    .swiper-item {
        flex: 1;
        flex-direction: row;
    }

    .scroll-v {
        flex: 1;
        /* #ifndef MP-ALIPAY */
        flex-direction: column;
        /* #endif */
        width: 750upx;
    }

    .update-tips {
        position: absolute;
        left: 0;
        top: 41px;
        right: 0;
        padding-top: 5px;
        padding-bottom: 5px;
        background-color: #FDDD9B;
        align-items: center;
        justify-content: center;
        text-align: center;
    }

    .update-tips-text {
        font-size: 14px;
        color: #ffffff;
    }

    .refresh {
        width: 750upx;
        height: 64px;
        justify-content: center;
    }

    .refresh-view {
        flex-direction: row;
        flex-wrap: nowrap;
        align-items: center;
        justify-content: center;
    }

	.refresh-icon {
		width: 30px;
		height: 30px;
		transition-duration: .5s;
		transition-property: transform;
		transform: rotate(0deg);
		transform-origin: 15px 15px;
	}

	.refresh-icon-active {
		transform: rotate(180deg);
	}

	.loading-icon {
		width: 20px;
		height: 20px;
		margin-right: 5px;
		color: #999999;
	}

    .loading-text {
        margin-left: 2px;
        font-size: 16px;
        color: #999999;
    }

    .loading-more {
        align-items: center;
        justify-content: center;
        padding-top: 10px;
        padding-bottom: 10px;
        text-align: center;
    }

    .loading-more-text {
        font-size: 28upx;
        color: #999;
    }
	
	
</style>
