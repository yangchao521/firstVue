 <template>
	<div>
		<input type="text" v-model="name">
		<p>{{name}}</p>
	</div>
 </template>

 <script>
 	export default{
 		name:'Form',
 		data(){
 			return{
 				name:'dsf'
 			}
 		},
 		watch:{
 			name:function(data){
 				console.log(data);
 			}
 		}
 	}
 </script>

 <style>
 
 </style>