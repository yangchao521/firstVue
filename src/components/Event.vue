<template>
	<!-- 在template中，有且只能有一个根容器 -->
	<div class="event">
		<ul>
			<li v-on:click="getItemInfo(index,$event)" v-for="(name,index) in names">{{ name }}</li>
		</ul>
		<input type="text" v-on:keyup.enter="getKeyInfo">
		<button v-on:click="pushArr">按钮</button>
		<button v-on:click="getOdd">我要奇数</button>
		<p>{{ msgRvs }}</p>
	</div>
</template>

<script type="text/javascript">
	export default{
		name: 'Event',
		data(){
			return {
				names:['asdf','adf','adsfr'],
				nums:[1,2,3,4,5,6,7,8,9,10],
				messages:"hello"
			}
		},
		methods:{
			getItemInfo(e,event){
				console.log(this.names[e])
				console.log(event)
			},
			getKeyInfo(e){
				console.log(e)
			},
			pushArr(){
				this.names.push("frank");
			},
			getOdd(){
				this.nums.filter(function(num){
					if(num % 2 !== 0){
						console.log(num)
					}
				})
			}
		},
		computed:{
			msgRvs () {
				return this.messages.split('').reverse().join('');
			}
		}
 	}
</script>

<style type="text/css">
	li{
		list-style: none;
	}
</style>