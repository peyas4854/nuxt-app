<template>
<div>
  
     <v-card v-for=" (users,index) in user " :key="index" class="mt-4">
        <v-list-item three-line>
        <v-list-item-content>
            <!-- <div class="overline mb-4">User name </div> -->
            <v-list-item-title class="headline mb-1">
                <N-link :to="'/user/'+users.id">  {{ users.name }}  </N-link>
               
                
        
            </v-list-item-title>
            <v-list-item-subtitle>{{ users.email}}</v-list-item-subtitle>
        </v-list-item-content>

        
        </v-list-item>

        <v-card-actions>
        <!-- <v-btn text>     
            <nuxt-link :to="'/user/'+users.id"> click </nuxt-link>
            </v-btn> -->
        
        </v-card-actions>
  </v-card>





</div>
</template>

<script>
import axois from "axios";

export default {
    head(){
        return{
            title:'User Page ',
            meta:[
                {hid:'description',
                name:'description',
                content:'Nuxt js Toodo Application'}
            ],
        }
    },
    data(){
        return{
            users:[],
        }
    },
    created(){
       // console.log("created");
        //this.allUser();
    },
//     methods: {
//           async allUser({ $axios }) {
//          const user = await $axios.$get('https://jsonplaceholder.typicode.com/user')	
//          return { user }
  
// }

        async asyncData({ $axios }) {
        const user = await $axios.$get('https://jsonplaceholder.typicode.com/users')
       // console.log(user);
        //this.users = user.data;
                
        return { user }
        // this.jokes = user;
        }
    }

   

</script>

<style scoped>
a{
    text-decoration: none;
    color:black;
}

</style>