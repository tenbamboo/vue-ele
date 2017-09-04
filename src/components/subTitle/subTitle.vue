<template>
	<div class="subTitle">
		<div class="line"></div>
		<div class="text">{{content}}</div>
		<div class="line"></div>
	</div>
</template>

<script>
export default {
	props:{
		content:{
			type:String
		}
	}
	// props:['content']
};
</script>

<style lang="stylus" rel="stylesheet/stylus">
	.subTitle
		display:flex
		width:80%
		margin: 28px auto 24px auto
		.line
			flex:2
			position:relative
			top: -6px
			border-bottom: 1px solid rgba(255,255,255,0.2)
		.text
			padding:0 12px
			font-size:14px
			font-weight:700
</style>