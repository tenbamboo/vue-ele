<template>
	<div class="goods">
		<div class="menu-wrapper"></div>
		<div class="foods-wrapper"></div>
	</div>
</template>

<script>
	const ERR_OK = 0;
	export default{
		props:{
			seller:{
				type:Object
			}
		},
		data(){
			return {
				goods:[]
			};
		},
		created(){
			this.$http.get('/api/goods').then((res) => {
		    	res = res.body;
		        if (res.errno === ERR_OK) {
		        	this.goods = res.data;
		        	console.log(this.goods);
		        }
		    });
		}
	};
</script>

<style lang="stylus" rel="stylesheet/stylus">
.goods
	position:absolute
	width:100%
	top:174px
	bottom:46px
	display:flex
	overflow:hidden
	.menu-wrapper
		flex: 0 0 80px
		width:80px
		background:#f3f5f7
	.foods-wrapper
		flex : 1


</style>

