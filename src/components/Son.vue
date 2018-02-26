<template>
	<div>
		儿子:{{ num * 3 }}
	</div>
</template>

<script>
	export default{
		name: 'son',
		data () {
			return {

			}
		},
		props: {
			message: String,
			num: Number
		}
	}
</script>

<style>

</style>