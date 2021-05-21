<template>
	<view class="content">
		<swiper class="swiper" :autoplay="false" :circular="true" next-margin="160rpx">
			<swiper-item v-for="(s,i) in sipwerList" :key="i">
				<view class="swiper-item">
					<image :src="s"></image>
				</view>
			</swiper-item>
		</swiper>
	</view>
</template>

<script>
	export default {
		data() {
			const image1 = require("../../static/1.png");
			const image2 = require("../../static/2.png");
			return {
				sipwerList: [image1, image2,image1,image2]
			}
		},
		onLoad() {
			console.log(this.sipwerList);
		},
		methods: {

		}
	}
</script>

<style>
	.content {
		display: flex;
		flex-direction: column;
		align-items: center;
		justify-content: center;
	}
	.swiper{
		margin-top: 60rpx;
		height: 300rpx;
		width: 100%;
	}
	.swiper-item{
		width: 549rpx;
		height: 291rpx;
	}
	::v-deep .swiper-item uni-image{
		width: 100%;
		height: 100%;
	}
</style>
