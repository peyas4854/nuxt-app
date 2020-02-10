<template>
<v-container>
   <v-flex xs12>
    <div>
      <h1> I am pages index </h1>
    
</div>
  </v-flex>
 </v-container>
</template>

<script>
import axois from "axios"
export default{
data(){
	return{
		
	}
},
async asyncData({ $axios }) {
  const user = await $axios.$get('https://jsonplaceholder.typicode.com/posts')
  //console.log(user);
		
  return { user }
  // this.jokes = user;
}

// async created(){
// 	const config={
// 		header:{
// 			Accept:"applicatio/json"
// 		}
// 	};
// 	try{
// 		const res = await $axios.$get(`https://jsonplaceholder.typicode.com/users`,config);
// 		console.log("try");

// 	}catch{
// 		console.log("catch");
// 	}
// }

 //  async created(context){
 // 	context.$axois.$get(`https://jsonplaceholder.typicode.com/users`)
 // 	.then(res => console.log(res))

 // }
}
</script>
<style scoped>	

</style>
