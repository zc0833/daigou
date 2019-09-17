<script>
	export default {
		onLaunch: function() {
			console.log('App Launch')
		},
		onShow: function() {
			console.log('App Show')
		},
		onHide: function() {
			console.log('App Hide')
		}
	}
</script>

<style>
	/*每个页面公共css */
	page{
		min-height: 100vh;
	}
	view{
		display: flex;
		flex-direction: column;
		/* justify-content: center; */
		align-items: center;
		box-sizing: border-box;
	}
</style>
