<template>
	<view>
		<!-- 搜索及tab -->
		<view class="searchBox">
			<input placeholder="请输入商品名或ID"/>
			<view class="Tab">
				<view class="TabList" v-for="(item,index) in list" :key="index"  :class="currentStyle==index?'onChoose':''" @click="changeClass(index)">
					<text>{{item.tittle}}</text>
				</view>
			</view>
		</view>
		<!-- 搜索及tab -->
		<swiper class="swiper"  :current="currentStyle" @change="changeRes">
			<swiper-item class="swiper-item" v-for="(item,index) in oderList" :key="index">
				<scroll-view scroll-y>
				<view v-for="(items,index) in item"  :key="index" class="orderListBlock">
					
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
			changeRes(e){
				
				this.currentStyle=e.target.current;
				console.log(this.currentStyle);
			},
			changeClass(i){
				console.log(i);
				this.currentStyle=i;
			}
		}
	}
</script>

<style>
.searchBox{
	width: 100%;
	height:210upx;
	background-color:#F1F1F1;
	display: flex;
	flex-direction: row;
	justify-content: center;
	align-content: center;
	display: flex;
	flex-direction: column;
	justify-content: space-around;
	
}
.searchBox input{
	width:90%;
	height:80upx;
	background-color: #FFFFFF;
	border-radius:50upx;
	font-size: 30upx;
}
.Tab{
	width:100%;
	height:100upx;
	background-color: #FFFFFF;
	display: flex;
	flex-direction: row;
	justify-content: space-around;
}
.TabList{
	font-size:28upx;
}
.swiper{
	width:100%;
	height:calc(100vh - 210upx);
	background-color:#F1F1F1; 
}
.orderListBlock{
	width:96%;
	height:400upx;
	background-color: #FFFFFF;
	border-radius: 20upx;
	margin:12upx auto 0 auto;
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
.swiper-item scroll-view{
	height: calc(100vh - 210upx);
}
.onChoose{
	color: red;
}
</style>
