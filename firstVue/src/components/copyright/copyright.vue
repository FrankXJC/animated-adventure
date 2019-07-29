<template>
	<div id="copyright">
		<!-- qqmusic -->
		<div class="brand">
			<img class='brand__logo' :src="rohlinLogo" alt="">
			<p class="brand__name">开发者rohlin-vue首次实战模仿</p>
			<p class="brand__name">联系邮箱:1666584574@qq.com</p>
		</div>	
	</div>
</template>
<script>
	export default{
		name:'copyright',
		data(){
			return{
				rohlinLogo:require('@/assets/rohlin_logo.jpg')
			}
		}
	}
</script>
<style scoped>
	.brand{
		padding:20px 0px;
		background:#fff;
	}
	.brand__logo{
		display: block;
	    width: 100px;
	    height: 100px;
	    margin: 0 auto;
	    border-radius:50%;
	}
	.brand__name{
		margin-top: 12px;
	    text-align: center;
	    font-size: 14px;
	    font-weight: 400;
	    color: #ccc;
	}
</style>