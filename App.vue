<script>
	export default {
		onLaunch: function() {
			uni.request({
				url: '/api/get/specifyUrl', //仅为示例，并非真实接口地址。
				// url: 'http://114.29.252.52:3000/api/get/specifyUrl',
				data: {
					name: '亚马逊'
				},
				success: (res) => {
					uni.setStorage({
						key: 'appUrl',
						data: res.data.data.url,
					});
				}
			});
		},
		onShow: function() {
			console.log('App Show')
		},
		onHide: function() {
			console.log('App Hide')
		}
	}
</script>

<style lang="scss">
	/* 注意要写在第一行，同时给style标签加入lang="scss"属性 */
	@import "@/uni_modules/uview-ui/index.scss";

	page {
		background-color: #f8f8f8;
	}
</style>