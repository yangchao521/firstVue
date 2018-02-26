<template>
	<div>
		我是自定义组件
		<Son />
	</div>
</template>

<script type="text/javascript">
	import Son from './Son.vue'
	export default{
		name:'mc',
		data(){
			return{

			}
		},
		components:{
			Son
		}
	}
</script>

<style>

</style>