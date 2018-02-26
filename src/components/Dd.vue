<template>
	<div>
		<p v-bind:class="{ active: isActive }">哈哈</p>
	</div>
</template>

<script>
	export default {
		name:'Dd',
		data () {
			return{
			msg:"hello vue!",
			isActive:true
			}
		}
	}
</script>

<style type="text/css">
	.active{
		color:red;
	}
</style>