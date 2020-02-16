<template>
		<view>		<view class="topTab"></view>		<view class="goback">			<img src="" />		</view>		<view class="cent">			<view class="mimages"></view>			<view class="mname">不足为害</view>		</view>		<view class="mcollect">			<view class="mycoll">我的收藏</view>			<view class="mright"><uni-icons type="arrowright" size="20"></uni-icons></view>		</view>		<view class="mcollect">			<view class="mycoll">消息中心</view>			<view class="mright"><uni-icons type="arrowright" size="20"></uni-icons></view>		</view>		<view class="myTab">			<view>				<view><uni-icons type="eye" size="40"></uni-icons></view>				<view>夜间模式</view>			</view>			<view>				<view><a herf="#"><uni-icons type="gear" size="40"></uni-icons></a></view>				<view>设置</view>			</view>		</view>	</view>
</template>

<script>
	import uniIcons from "@/components/uni-icons/uni-icons.vue"
	export default {
		components: {uniIcons},
		data() {
			return {
			}
		},
		onLoad() {
	
		},
		methods: {
		 }
}
</script>

<style>
	.topTab{		height:20px;		width: 100%;	}	.goback{		padding:0 15px ;		width: 100%;		height: 30px;		text-align: left;	}	.goback img{		width: 25px;	}	.mimages{		width: 80px;		height: 80px;		border-radius: 50px;		background-color: #42B983;		margin: 0 auto;		/* display: none; */	}	.cent{		width: 100%;		/* background-color: #FFAABB; */		margin-bottom: 20px;	}	.mname{		width: 100%;		margin: 0 auto;		font-weight: bold;		line-height: 40px;		font-size: 20px;
		text-align: center;	}	.mcollect{		border-top: 1px solid #F6F6F6;		display: flex;		padding: 15px 10px;			}	.mycoll{		font-size: 18px;			}	.mright{		position: absolute;		right: 20px;	}	.myTab{		display: flex;		justify-content:space-around;		position: absolute;		bottom: 40px;		width: 100%;	}
</style>
