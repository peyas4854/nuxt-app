<template>
  <v-container>

  <div>
  	 <h2> {{ route }} </h2>
  	<!--  <h2> {{ post }} </h2> -->
  </div>

     </v-container> 
</template>

<script>
export default {

  data(){
    return{
      route:this.$route.params.index,
    }
  },
 async asyncData({ $axios,$route }) {
 	//const id = this.$route.params.index;
  // const post = await $axios.$get(`https://jsonplaceholder.typicode.com/posts/this.route`)
 // console.log(id);
		
  // return { post }
  // this.jokes = user;
}

}
</script>
