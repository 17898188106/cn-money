<template>
	<view class="content">
		<view class="header">
			<image class="logo" src="/static/logo.png"></image>
		</view>
		
		<uni-section title="价格扩展" type="line"></uni-section>
		<uni-list>
			<uni-list-item title="默认">
				<template slot="footer">
					<cn-money :money="52013.14"></cn-money>
				</template>
			</uni-list-item>
			<uni-list-item title="加大主字体">
				<template slot="footer">
					<cn-money :money="9168.45" :size="48"></cn-money>
				</template>
			</uni-list-item>
			<uni-list-item title="颜色">
				<template slot="footer">
					<cn-money :money="4168.25" :size="38" color="#9397a4"></cn-money>
				</template>
			</uni-list-item>
			<uni-list-item title="删除线">
				<template slot="footer">
					<cn-money :money="7168.39" color="#9397a4" original></cn-money>
				</template>
			</uni-list-item>
			<uni-list-item title="显示千分位">
				<template slot="footer">
					<cn-money :money="16852013.14" thousandth></cn-money>
				</template>
			</uni-list-item>
			<uni-list-item title="零小数不显示(168.00)">
				<template slot="footer">
					<cn-money :money="168.00" :size="38" :showZeroDecimal="false"></cn-money>
				</template>
			</uni-list-item>
			<uni-list-item title="单位($)">
				<template slot="footer">
					<cn-money :money="168.47" :size="38" unit="$"></cn-money>
				</template>
			</uni-list-item>
			<uni-list-item title="单位不显示">
				<template slot="footer">
					<cn-money :money="168.52" :size="38" :showUnit="false"></cn-money>
				</template>
			</uni-list-item>
			<uni-list-item title="人民币(¥168.39)">
				<template slot="footer">
					<cn-money :money="168.39" rmb></cn-money>
				</template>
			</uni-list-item>
			<uni-list-item title="人民币(¥502.00)">
				<template slot="footer">
					<cn-money :money="502.00" rmb></cn-money>
				</template>
			</uni-list-item>
		</uni-list>
	</view>
</template>

<script>
	import cnMoney from '@/components/cn-money/cn-money.vue';
	
	export default {
		components:{
			cnMoney
		},
		data() {
			return {
				title: 'Hello'
			}
		},
		onLoad() {

		},
		methods: {

		}
	}
</script>

<style>
	/* #ifndef APP-NVUE */
	page {
		display: flex;
		flex-direction: column;
		box-sizing: border-box;
		background-color: #F8F8F8;
		min-height: 100%;
		height: auto;
	}
	
	view {
		font-size: 14px;
		line-height: inherit;
	}
	/* #endif */
	
	.content {
		width: 100%;
		display: flex;
		flex-direction: column;
		box-sizing: border-box;
	}
	
	.header{
		width: 100%;
		box-sizing: border-box;
		background-color: #FFFFFF;
		overflow: hidden;
		display: inline-flex;
		align-items: center;
		justify-content: center;
	}
	
	.logo {
		height: 100rpx;
		width: 100rpx;
		margin-top: 50rpx;
		margin-left: auto;
		margin-right: auto;
		margin-bottom: 50rpx;
	}
	
	.slot-box {
		/* #ifndef APP-NVUE */
		display: flex;
		/* #endif */
		flex-direction: row;
		align-items: center;
	}

	.slot-image {
		/* #ifndef APP-NVUE */
		display: block;
		/* #endif */
		margin-right: 10px;
		width: 30px;
		height: 30px;
	}

	.slot-text {
		flex: 1;
		font-size: 14px;
		color: #4cd964;
		margin-right: 10px;
	}
</style>
