<template>
	<view>
		<view class="header">
			<view class="header_content">
				<text class="title">HI,Xxxxxx</text>
			</view>
		</view>
		<image class="logo" src="../../static/banner.png"></image>
		<!-- 订单管理 -->
		<view class="orderManagement">
			<view class="orderTitle" @click="go()"><view>订单管理</view><view>></view></view>
			<view class="orderState">
				<view><view>0</view><view>待付款</view></view>
				<view><view>0</view><view>待付款</view></view>
				<view><view>0</view><view>待付款</view></view>
				<view><view>1</view><view>退款售后</view></view>
			</view>
		</view>
	<!-- 订单管理 -->
	<!-- 商品管理 -->
		<view class="orderManagement  commodityManagement ">
			<view class="orderTitle" @click="xixi()"><view>商品管理</view><view>></view></view>
			<view class="orderState">
				<view><view>0</view><view>待付款</view></view>
				<view><view>0</view><view>待付款</view></view>
				<view><view>0</view><view>待付款</view></view>
				<view><view>1</view><view>退款售后</view></view>
			</view>
		</view>
	<!--商品管理 -->
	<!-- 四个图 -->
	<view class="image">
		<view v-for="(item,index) in list" :key=index>
			<image :src="item.src_path"></image>
			<view>{{item.tittle}}</view>
		</view>
	</view>
	<!-- 四个图 -->
	
	</view>
</template>

<script>
	export default {
		data() {
			return {
				list:[
					{
						tittle:"需求管理",
						src_path:"../../static/xqgl.png"
					},
					{
						tittle:"数据统计",
						src_path:"../../static/sjtj.png"
					},
					{
						tittle:"营销推广",
						src_path:"../../static/yxtg.png"
					},
					{
						tittle:"规则中心",
						src_path:"../../static/gjzx.png"
					}
				]
			}
		},
		onLoad() {

		},
		methods: {
				go:function(){
					console.log("55");
					uni.navigateTo({
					    url: '../orderList/orderList'
					});
				},
				// go1:function(){
				// 	console.log("55");
				// 	uni.navigateTo({
				// 	    url: '../commodityManagement/commodityManagement'
				// 	});
				// }
				xixi:function(){
					uni.getNetworkType({
					    success: function (res) {
					        console.log(res.networkType);
					    }
					});
				}
				
		}
	}
</script>

<style>

	.header{
		width:100%;
		height:80upx;
	}
	.header_content{
		width:100%;
		height:80upx;
		line-height: 100upx;
		background-color: #C8C7CC;
		color:#4CD964;
		padding-left: 40upx;
		padding-bottom: 10upx;
	}
	.logo{
		width:100%;
		height:328upx;
	}
	.orderManagement{
		width:90%;
		height:220upx;
		background-color:#C8C7CC;
		border-radius:20upx;
		margin-top:-20upx;
		display: flex;
		flex-direction:column;
		justify-content:space-between;
	}
	.orderTitle:nth-child(1){
		font-size:35upx;
	}
	.orderTitle{
		width:100%;
		padding:0 25upx;
		display: flex;
		flex-direction: row;
		justify-content:space-between;
	}
	.orderState{
		width:100%;
		height:150upx;
		background-color: #C0C0C0;
		display: flex;
		flex-direction: row;
		justify-content: space-around;
		font-size:28upx;
		border-radius:20upx;
		border-radius:20upx;		
	}
	.commodityManagement{
		margin-top: 30upx;
	}
	.image{
		background-color: #C8C7CC;
		width:90%;
		height:228upx;
		border-radius: 20upx;
		margin-top:30upx;
		flex-direction: row;
		align-items: center;
		justify-content: space-between;
		padding: 0 30upx;
		
	}
	.image view image{
		height:100upx;
		width:100upx;
	}
	.image view view{
		font-size: 24upx;
	}
</style>
