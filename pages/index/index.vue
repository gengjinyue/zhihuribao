<template>
	<view class="content">
		<view class="text-nav">
			<view class="navLeft">
				111
			</view>
			<text class="space">|</text>
			<text class="navTitle">知乎日报</text>
			<view class="navRight">
				<navigator url="../people/people" open-type="navigate"><uni-icons type="contact" size="30"></uni-icons></navigator>
			</view>
		</view>
			<!-- <view class="uni-padding-wrap">
				<view class="page-section swiper">
					<view class="page-section-spacing">
						<swiper class="swiper" :indicator-dots="indicatorDots" :autoplay="autoplay" :interval="interval" :duration="duration">
							<swiper-item>
								<view class="swiper-item uni-bg-red">A</view>
							</swiper-item>
							<swiper-item>
								<view class="swiper-item uni-bg-green">B</view>
							</swiper-item>
							<swiper-item>
								<view class="swiper-item uni-bg-blue">C</view>
							</swiper-item>
						</swiper>
					</view>
				</view>
			</view> -->
			<view class="banner">
				<swiper class="swiper" indicator-color="rgba(255, 255, 255, 0.6)" indicator-active-color="rgba(255, 255, 255, 1)"
				 :autoplay="true" :interval="3000" :duration="1000" :current="swiperCurrent" @change="changeSwiper">
					<swiper-item v-for="item in swiperImg" :key="item.id">
						<image class="swiper-item" :src="item" mode="widthFix" style="height:600rpx;"></image>
					</swiper-item>
				</swiper>
				<view class="dots">
					<block v-for="(item,index) in swiperImg.length" :key="item.id">
						<view class="dot" :class="index==swiperCurrent ? ' active' : ''"></view>
					</block>
				</view>
			</view>
		<view class="indexList" >
			<view class="fistList">
				<view class="listLeft">
					<text class="leftTile">明明很多中国人皮肤不算黄色？</text>
					<text class="leftText"> 情报员 3分钟</text>
				</view>
				<view class="listRt">
					<image src="../../static/logo.png" mode="" ></image>
				</view>
			</view>
			<view class="fistList">
				<view class="listLeft">
					<text class="leftTile">明明很多中国人皮肤不算黄色？</text>
					<text class="leftText"> 情报员 3分钟</text>
				</view>
				<view class="listRt">
					<image src="../../static/logo.png" mode="" ></image>
				</view>
			</view>
			<view class="fistList">
				<view class="listLeft">
					<text class="leftTile">明明很多中国人皮肤不算黄色？</text>
					<text class="leftText"> 情报员 3分钟</text>
				</view>
				<view class="listRt">
					<image src="../../static/logo.png" mode="" ></image>
				</view>
			</view>
		</view>
	</view>
</template>

<script>
	import uniIcons from "@/components/uni-icons/uni-icons.vue"
	export default {
		components: {uniIcons},
		data() {
			return {
				// data:new Date().toISOString().slice(0, 10),
				// background: [],
				// indicatorDots: true,
				// autoplay: true,
				// interval: 2000,
				// duration: 500
			swiperImg: [
				'../../static/swiper.png',					
				'../../static/swiper1.png',
				'../../static/swiper.png'
			],
			none: true,
			current: 0,
			mode: 'default',
			swiperCurrent: 0,
			}
			},
		onLoad() {

		},
		methods: {
		    changeSwiper(e) {
		    	this.swiperCurrent = e.detail.current;
		    }
		 }
	}
</script>
<style lang="scss">
	.content {
		.text-nav{
			/* background-color: red; */
			height: 100rpx;
		}
		.space{
			padding: 0 10rpx;
			color: #999;
			line-height: 100rpx;
		}
		.navTitle{
			font-size: 40rpx;
		}
		.navLeft{
			float: left;
			width: 10%;
			font-size: 30rpx;
			line-height: 100rpx;
		}
		.navRight{
			float: right;
			width: 10%;
			line-height: 100rpx;
		}
		.banner{
			.swiper {
				width: 100%;
				height: 500rpx;
				border-radius: 16rpx;
				overflow: hidden;
				margin-top: 16rpx;
				position: relative;
				background: yellow;
				.swiper-item {
					width: 100%;
					height: 500rpx;
				}
			}
			.dots {
				position: absolute;
				top: 600rpx;
				left: 80%;
				transform: translate(-50% 0);
				z-index: 4;
				display: flex;
				justify-content: center;
			
				.dot {
					width: 24rpx;
					height: 8rpx;
					transition: all .6s;
					background: rgba(0, 0, 0, .3);
					margin-right: 10rpx;
				}
			
				.active {
					width: 24rpx;
					height: 8rpx;
					background: rgba(255, 255, 255, .8);
				}
			}
		}
		.indexList{
			margin-top: 20rpx;
			overflow: hidden;
			padding-left: 30rpx;
			.fistList{
				height: 200rpx;
				overflow: hidden;
				.listLeft{
					float: left;
					width: 77%;
					.leftTile{
						padding-top: 20rpx;
						font-size: 40rpx;
						display: block;
					}
					.leftText{
						font-size: 30rpx;
						color: #C0C0C0;
					}
				}
				.listRt{
					float: right;
					width: 20%;
					line-height: 200rpx;
					image{
						height: 120rpx;
						width: 120rpx;
						vertical-align: middle;
					}
				}
			}
		}
	}
</style>
