<template>
	<view>
		<view class="background">
			<view class="pageT">
				<view class="time">
					
				</view>
				<view class="orderTab">
					<view class="orderTabList" v-for="(item,index) in list" :key="index" :class="currentStyle==index?'onChoose':''" @click="onChooseTab(index)">
						<text>{{item.tittle}}</text>
					</view>
				</view>
			</view>
			<swiper class="swiper" :interval="3000" :duration="300" :current="currentStyle" @change="currentChange">
				<swiper-item class="swiper-item" v-for="(item,index) in oderList" :key="index">
					<scroll-view scroll-y>
						<view class="orderListBlock"  v-for="(items,indexs) in item" :key="indexs">
							<view class="top">
								<view>{{items.orderNumber}}</view>
								<view>{{items.orderStatus}}</view>
							</view>
							<view class="center">
								<image :src="items.src_path"></image>
								<view>
									<view>{{items.commodityTitle}}</view>
									<view class="guige">
										<view>{{items.specification}}</view>
										<view>x1</view>
									</view>
									<view>{{items.price}}</view>
								</view>
							</view>
						</view>
					</scroll-view>
				</swiper-item>
			</swiper>
		</view>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				currentStyle:0,
				list:[
					{
						tittle:"全部"
					},
					{
						tittle:"待付款"
					},
					{
						tittle:"待发货"
					},
					{
						tittle:"待收货"
					},
				],
				oderList:[
					[
						{
							orderNumber:201909150915,		    //订单号
							src_path:"../../static/jcw.png"	,   //图
							orderStatus:"已关闭",				//订单状态
							commodityTitle:"xxxxxxxxxxxxxxx"	,//商品标题
							specification:"无规格",					//规格
							price:"$10",							//价格
							numberOfCases:"1",			//件数
							time:"2019-09-14  15:56:21"//下单时间
						},
						{
							orderNumber:201909150915,		    //订单号
							src_path:"../../static/jcw.png"	,   //图
							orderStatus:"已关闭",				//订单状态
							commodityTitle:"xxxxxxxxxxxxxxx"	,//商品标题
							specification:"无规格",					//规格
							price:"$10",							//价格
							numberOfCases:"1",			//件数
							time:"2019-09-14  15:56:21"//下单时间
						},
						{
							orderNumber:201909150915,		    //订单号
							src_path:"../../static/jcw.png"	,   //图
							orderStatus:"已关闭",				//订单状态
							commodityTitle:"xxxxxxxxxxxxxxx"	,//商品标题
							specification:"无规格",					//规格
							price:"$10",							//价格
							numberOfCases:"1",			//件数
							time:"2019-09-14  15:56:21"//下单时间
						},
						{
							orderNumber:201909150915,		    //订单号
							src_path:"../../static/jcw.png"	,   //图
							orderStatus:"已关闭",				//订单状态
							commodityTitle:"xxxxxxxxxxxxxxx"	,//商品标题
							specification:"无规格",					//规格
							price:"$10",							//价格
							numberOfCases:"1",			//件数
							time:"2019-09-14  15:56:21"//下单时间
						},
						{
							orderNumber:201909150915,		    //订单号
							src_path:"../../static/jcw.png"	,   //图
							orderStatus:"已关闭",				//订单状态
							commodityTitle:"xxxxxxxxxxxxxxx"	,//商品标题
							specification:"无规格",					//规格
							price:"$10",							//价格
							numberOfCases:"1",			//件数
							time:"2019-09-14  15:56:21"//下单时间
						}
					],[
						{
							orderNumber:201909150915,		    //订单号
							src_path:"../../static/jcw.png"	,   //图
							orderStatus:"已关闭",				//订单状态
							commodityTitle:"xxxxxxxxxxxxxxx"	,//商品标题
							specification:"无规格",					//规格
							price:"$10",							//价格
							numberOfCases:"1",			//件数
							time:"2019-09-14  15:56:21"//下单时间
						},
						{
							orderNumber:201909150915,		    //订单号
							src_path:"../../static/jcw.png"	,   //图
							orderStatus:"已关闭",				//订单状态
							commodityTitle:"xxxxxxxxxxxxxxx"	,//商品标题
							specification:"无规格",					//规格
							price:"$10",							//价格
							numberOfCases:"1",			//件数
							time:"2019-09-14  15:56:21"//下单时间
						},
						{
							orderNumber:201909150915,		    //订单号
							src_path:"../../static/jcw.png"	,   //图
							orderStatus:"已关闭",				//订单状态
							commodityTitle:"xxxxxxxxxxxxxxx"	,//商品标题
							specification:"无规格",					//规格
							price:"$10",							//价格
							numberOfCases:"1",			//件数
							time:"2019-09-14  15:56:21"//下单时间
						},
						{
							orderNumber:201909150915,		    //订单号
							src_path:"../../static/jcw.png"	,   //图
							orderStatus:"已关闭",				//订单状态
							commodityTitle:"xxxxxxxxxxxxxxx"	,//商品标题
							specification:"无规格",					//规格
							price:"$10",							//价格
							numberOfCases:"1",			//件数
							time:"2019-09-14  15:56:21"//下单时间
						},
						{
							orderNumber:201909150915,		    //订单号
							src_path:"../../static/jcw.png"	,   //图
							orderStatus:"已关闭",				//订单状态
							commodityTitle:"xxxxxxxxxxxxxxx"	,//商品标题
							specification:"无规格",					//规格
							price:"$10",							//价格
							numberOfCases:"1",			//件数
							time:"2019-09-14  15:56:21"//下单时间
						}
					],[
						{
							orderNumber:201909150915,		    //订单号
							src_path:"../../static/jcw.png"	,   //图
							orderStatus:"已关闭",				//订单状态
							commodityTitle:"xxxxxxxxxxxxxxx"	,//商品标题
							specification:"无规格",					//规格
							price:"$10",							//价格
							numberOfCases:"1",			//件数
							time:"2019-09-14  15:56:21"//下单时间
						},
						{
							orderNumber:201909150915,		    //订单号
							src_path:"../../static/jcw.png"	,   //图
							orderStatus:"已关闭",				//订单状态
							commodityTitle:"xxxxxxxxxxxxxxx"	,//商品标题
							specification:"无规格",					//规格
							price:"$10",							//价格
							numberOfCases:"1",			//件数
							time:"2019-09-14  15:56:21"//下单时间
						},
						{
							orderNumber:201909150915,		    //订单号
							src_path:"../../static/jcw.png"	,   //图
							orderStatus:"已关闭",				//订单状态
							commodityTitle:"xxxxxxxxxxxxxxx"	,//商品标题
							specification:"无规格",					//规格
							price:"$10",							//价格
							numberOfCases:"1",			//件数
							time:"2019-09-14  15:56:21"//下单时间
						},
						{
							orderNumber:201909150915,		    //订单号
							src_path:"../../static/jcw.png"	,   //图
							orderStatus:"已关闭",				//订单状态
							commodityTitle:"xxxxxxxxxxxxxxx"	,//商品标题
							specification:"无规格",					//规格
							price:"$10",							//价格
							numberOfCases:"1",			//件数
							time:"2019-09-14  15:56:21"//下单时间
						},
						{
							orderNumber:201909150915,		    //订单号
							src_path:"../../static/jcw.png"	,   //图
							orderStatus:"已关闭",				//订单状态
							commodityTitle:"xxxxxxxxxxxxxxx"	,//商品标题
							specification:"无规格",					//规格
							price:"$10",							//价格
							numberOfCases:"1",			//件数
							time:"2019-09-14  15:56:21"//下单时间
						}
					],[
						{
							orderNumber:201909150915,		    //订单号
							src_path:"../../static/jcw.png"	,   //图
							orderStatus:"已关闭",				//订单状态
							commodityTitle:"xxxxxxxxxxxxxxx"	,//商品标题
							specification:"无规格",					//规格
							price:"$10",							//价格
							numberOfCases:"1",			//件数
							time:"2019-09-14  15:56:21"//下单时间
						},
						{
							orderNumber:201909150915,		    //订单号
							src_path:"../../static/jcw.png"	,   //图
							orderStatus:"已关闭",				//订单状态
							commodityTitle:"xxxxxxxxxxxxxxx"	,//商品标题
							specification:"无规格",					//规格
							price:"$10",							//价格
							numberOfCases:"1",			//件数
							time:"2019-09-14  15:56:21"//下单时间
						},
						{
							orderNumber:201909150915,		    //订单号
							src_path:"../../static/jcw.png"	,   //图
							orderStatus:"已关闭",				//订单状态
							commodityTitle:"xxxxxxxxxxxxxxx"	,//商品标题
							specification:"无规格",					//规格
							price:"$10",							//价格
							numberOfCases:"1",			//件数
							time:"2019-09-14  15:56:21"//下单时间
						}
					]
				]
			}
		},
		methods: {
			currentChange(e){
				console.log(e.target.current);
				this.currentStyle = e.target.current;
			},
			onChooseTab(i){
				console.log(i);
				this.currentStyle = i;
			}
		}
	}
</script>

<style>
.background{
	width: 100%;
	height:100vh;
	background-color:#F1F1F1;
}
.onChoose{
	color: red;
}
.orderTab{
	width:100%;
	height:80upx;
	background-color:#FFFFFF;
}
.orderTab{
	display: flex;
	flex-direction: row;
	justify-content: space-around;
	font-size: 28upx;
}
.swiper{
	width: 100%;
	height: calc(100vh - 160upx);
}
.swiper-item{
	display: flex;
	flex-direction: column;
	justify-content: flex-start;
	align-items: center;
	width: 100vw;
}
.swiper-item scroll-view{
	height: calc(100vh - 160upx);
}
.orderListBlock{
	width:96%;
	height:400upx;
	background-color: #FFFFFF;
	border-radius: 20upx;
	margin-top:12upx;
	padding:0 30upx;
}
.top{
	width:100%;
	display: flex;
	flex-direction:row;
	justify-content:space-between;
	font-size:30upx;
}
.center{
	width:100%;
	display: flex;
	flex-direction: row;
	margin-top:40upx;
	justify-content:flex-start;
	font-size: 30upx;
/* 	background-color: #007AFF; */
}
.center image{
	min-width:140upx;
	width:140upx;
	height:140upx;
	margin-right: 50upx;
}
.center>view{
	height:100%;
	width:100%;
	display: flex;
	flex-direction: column;
	justify-content: space-between;
	align-items: flex-start;
}
.guige{
	width:100%;
	flex-direction: row;
	justify-content:space-between;
	align-items: center;
	/* background-color: #4CD964; */
}
.pageT{
	display: flex;
	flex-direction: column;
/* 	height:160upx; */
	width:100%;
}
.time{
	width:100%;
	height:80upx;
	background-color: #4CD964;
}
</style>
