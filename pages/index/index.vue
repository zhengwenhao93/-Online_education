<template>
	<view class="container">
		<!-- 头部搜索框 -->
		<i-search-bar></i-search-bar>

		<!-- 轮播图 -->
		<i-swiper :data="bannerData" @click="handleToDetail"></i-swiper>

		<!-- 导航栏 -->
		<i-nav :data="navList"></i-nav>

		<!-- 优惠卷 -->
		<i-coupon :data="couponList"></i-coupon>

		<!-- 背景线 -->
		<view class="divider"></view>

		<!-- 拼团 -->
		<view class="px-2">
			<i-list-title><template v-slot:title>拼团</template></i-list-title>
			<i-course-list :data="groupList" type="column"></i-course-list>
		</view>

		<view class="divider"></view>

		<!-- 最新列表 -->
		<view class="px-2">
			<i-list-title>
				<template v-slot:title>最新列表</template>
				<template v-slot:sub-title>查看全部</template>
			</i-list-title>
			<i-course-list :data="groupList" type="row"></i-course-list>
		</view>

		<view class="divider"></view>



		<view class="divider"></view>

		<view class="advert">
			<image src="../../static/demo/cover/1.png" mode="aspectFill"></image>
		</view>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				bannerData: [{
						course_id: 538,
						course_title: "VueCli 实战商城后台管理系统",
						src: "https://tangzhe123-com.oss-cn-shenzhen.aliyuncs.com/dishaweb/08C9150BC2B163AEC012D6E544C75DD2.png",
						type: "webview",
						url: "http://www.dishaxy.com"
					},
					{
						course_id: 538,
						course_title: "VueCli 实战商城后台管理系统",
						src: "https://tangzhe123-com.oss-cn-shenzhen.aliyuncs.com/dishaweb/96bd39ce1d334b8493bac12bb1aa4223.png",
						type: "course",
						url: ""
					}
				],

				navList: [{
					src: "/static/demo/icon/hd.png",
					name: "活动",
				}, {
					src: "/static/demo/icon/test.png",
					name: "考试",
				}, {
					src: "/static/demo/icon/ms.png",
					name: "秒杀",
				}, {
					src: "/static/demo/icon/pt.png",
					name: "拼团",
				}, {
					src: "/static/demo/icon/course.png",
					name: "直播",
				}, {
					src: "/static/demo/icon/column.png",
					name: "专栏",
				}, {
					src: "/static/demo/icon/book.png",
					name: "电子书",
				}, {
					src: "/static/demo/icon/ask.png",
					name: "社区",
				}],
				couponList: [{
						c_num: 300000,
						end_time: "2025-08-22T16:00:00.000Z",
						goods_id: 1636,
						id: 83,
						isgetcoupon: true,
						price: "4.00",
						received_num: 19,
						start_time: "2022-07-14T16:00:00.000Z",
						type: "course",
						value: {
							id: 1636,
							title: "中级经济法-知识点精讲课"
						}
					},
					{
						c_num: 10000,
						end_time: "2034-10-16T16:00:00.000Z",
						goods_id: 184,
						id: 39,
						isgetcoupon: false,
						price: "8.90",
						received_num: 141,
						start_time: "2021-09-09T16:00:00.000Z",
						type: "column",
						value: {
							id: 184,
							title: "VueCli 实战商城后台管理系统"
						}
					},
					{
						c_num: 100000,
						end_time: "2035-07-28T16:00:00.000Z",
						goods_id: 6,
						id: 33,
						isgetcoupon: false,
						price: "5.00",
						received_num: 121,
						start_time: "2021-06-28T17:58:01.000Z",
						type: "course",
						value: {
							id: 6,
							title: "VueCli 实战在线教育后台系统"
						}
					},
					{
						c_num: 100000,
						end_time: "2032-06-29T16:00:00.000Z",
						goods_id: 11,
						id: 19,
						isgetcoupon: false,
						price: "50.00",
						received_num: 88,
						start_time: "2021-05-15T17:03:00.000Z",
						type: "course",
						value: {
							id: 11,
							title: "uni-app实战直播app全栈开发"
						}
					},
					{
						c_num: 10000,
						end_time: "2032-06-29T16:00:00.000Z",
						goods_id: 12,
						id: 18,
						isgetcoupon: false,
						price: "5.00",
						received_num: 82,
						start_time: "2021-05-15T17:02:00.000Z",
						type: "course",
						value: {
							id: 12,
							title: "unicloud商城全栈开发"
						}
					}
				],
				groupList: [{
						cover: "http://demo-mp3.oss-cn-shenzhen.aliyuncs.com/egg-edu-demo/6dccd3181a1b973480ec.jpg",
						end_time: "2022-08-28T16:00:00.000Z",
						group_id: 184,
						id: 269,
						price: "0.10",
						start_time: "2022-07-20T16:00:00.000Z",
						t_price: "0.10",
						title: "33213",
						type: "column"
					}, {
						cover: "http://demo-mp3.oss-cn-shenzhen.aliyuncs.com/egg-edu-demo/f64e4441378d85f5df7a.png",
						end_time: "2022-08-21T16:00:00.000Z",
						group_id: 182,
						id: 1604,
						price: "0.10",
						start_time: "2022-07-13T16:00:00.000Z",
						t_price: "2.00",
						title: "123",
						type: "media"
					},
					{
						cover: "http://demo-mp3.oss-cn-shenzhen.aliyuncs.com/egg-edu-demo/d1c2fbe07e31d1e78b5a.png",
						end_time: "2024-06-01T13:26:31.000Z",
						group_id: 123,
						id: 1432,
						price: "43442.00",
						start_time: "2022-05-31T13:26:31.000Z",
						t_price: "0.00",
						title: "231",
						type: "media"
					}, {
						cover: "http://demo-mp3.oss-cn-shenzhen.aliyuncs.com/egg-edu-demo/b688b9bf339a6ece9f54.png",
						end_time: "2024-06-29T16:00:00.000Z",
						group_id: 31,
						id: 25,
						price: "0.10",
						start_time: "2021-05-16T08:31:00.000Z",
						t_price: "10.00",
						title: "uni-app实战在线教育类app开发",
						type: "audio"
					},
					{
						cover: "http://demo-mp3.oss-cn-shenzhen.aliyuncs.com/egg-edu-demo/2e96031726768d0d493f.png",
						end_time: "2024-06-22T16:00:00.000Z",
						group_id: 30,
						id: 3,
						price: "50.00",
						start_time: "2021-05-15T17:05:00.000Z",
						t_price: "9.98",
						title: "uni-app实战仿微信app开发",
						type: "column"
					},
					{
						cover: "http://demo-mp3.oss-cn-shenzhen.aliyuncs.com/egg-edu-demo/10ccf3a973f5193bec3c.png",
						end_time: "2024-06-29T16:00:00.000Z",
						group_id: 29,
						id: 6,
						price: "5.00",
						start_time: "2021-05-15T17:04:00.000Z",
						t_price: "9.98",
						title: "VueCli 实战在线教育后台系统",
						type: "media"
					},
					{
						cover: "http://demo-mp3.oss-cn-shenzhen.aliyuncs.com/egg-edu-demo/c948f4a7e402473337cb.png",
						end_time: "2024-06-29T16:00:00.000Z",
						group_id: 21,
						id: 11,
						price: "8.00",
						start_time: "2021-04-15T16:00:00.000Z",
						t_price: "90.00",
						title: "uni-app实战直播app全栈开发",
						type: "video"
					}
				]
			}
		},
		methods: {
			/** 点击轮播图跳转到详情页
			 * @param {Object} item
			 */
			handleToDetail(item) {
				// TODO 点击跳转到对应的详情页面, 并且还需要将id传过去
				console.log(item)
			}
		}
	}
</script>

<style>
	.advert {
		width: 750rpx;
		height: 360rpx;
	}
</style>
