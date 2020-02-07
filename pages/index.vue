<template>
<v-container>

   <v-flex xs12>
    <div>
    	<v-simple-table>
    
      <thead>
        <tr>

          <th class="text-left">   title   </th>


          <th class="text-left">Email</th>
          <th class="text-left">Phone</th>
        </tr>
      </thead>
      <tbody>
        <tr v-for="(item,index) in user" :key="index">

        	
        	   <td> <N-link class="link" :to="'employee/'+ item.id" text > {{ item.title }} 	</N-link></td>
        
          

          <td>{{ item.email }}</td>
          <td>{{ item.phone }}</td>
         
        </tr>
      </tbody>
  </v-simple-table>
    

    	
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
.link{
	text-decoration:none;
	color:black!important;
}
</style>
