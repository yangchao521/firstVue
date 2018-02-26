<template>
	<div>
		<input type="text" name="" v-model="feng">
		<Son :message="feng"></Son>
		<input type="text" name="" v-model.number="num">
		<Son :num="num"></Son>
	</div>
</template>

<script type="text/javascript">
	import Son from './Son.vue'
	export default{
		name:'mc',
		data () {
			return{
				msg:"我是活的数据",
				feng:"",
				num:10
			}
		},
		components:{
			Son
		}
	}
</script>

<style>

</style>