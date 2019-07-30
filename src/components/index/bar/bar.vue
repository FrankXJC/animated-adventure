<template>
	<div id='bar'>
		<ul class="bar_ul">
			<slot></slot>
		</ul>
	</div>
</template>
<script>
	export default{
		name:'bar',
		
	}
</script>
<style scoped>
	.bar_ul{
		background:#fff;
		display:flex;
	}
	.bar_ul li{
		flex-grow:1;
		height:38px;
		line-height:38px;
		color:rgba(0,0,0,.6);
		text-align: center;
		font-size:16px;
		border-bottom:2px solid #fff;
	}
	
</style>