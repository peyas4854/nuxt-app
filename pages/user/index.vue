<template>
<div>
    
<v-row>
    <v-col md="6">
   <p class="mr-2">Order by </p>
    
        <v-btn class="mr-2" small @click="sortBy('Asending')">Asending</v-btn>
   
        <v-btn small @click="sortBy('Desending')">Desending</v-btn>
    </v-col>
    <v-col md="6">
<v-select
          :items="items"
          label="limit"
          v-model="limits"
          @change="limit"
        ></v-select>
    </v-col>
 
   
    
   
</v-row>
 
  

         <v-text-field
            label="Search"
            single-line
            solo
            v-model="search"
          > </v-text-field>
          <!-- <v-btn @click="searchUser" small color="primary">Search</v-btn> -->

     <v-card v-for=" (users,index) in  userfilter " :key="index" class="mt-4">
        <v-list-item three-line>
        <v-list-item-content>
           
            <v-list-item-title class="headline mb-1">
                <N-link :to="'/user/'+users.id">  {{ users.name | capitalize }}  </N-link>
               
                
        
            </v-list-item-title>
            <v-list-item-subtitle>{{ users.email }}</v-list-item-subtitle>
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
           
            search:'',
             items: [2, 4, 6, 8],
             limits:'',
        }
    },
    async asyncData({ $axios }) {
    const user = await $axios.$get('https://jsonplaceholder.typicode.com/users')        
    return { user }
    
    },
    computed:{
        userfilter(){
            if( this.search.trim() !=''){
                return  this.user.filter(c=> c.name.toLowerCase().includes(this.search.toLowerCase()));      
            }
            return this.user;
        }
    },
    methods:{
        sortBy(props){
            if(props =='Asending'){
            return this.user.sort((a,b)=>a.id >b.id  ? -1 :1)
            }else{
            return this.user.reverse();
            }
        },

        limit(){
            console.log("limit",Object.keys(this.user));

        }
    },


    filters:{
        capitalize(user){
            return user.toUpperCase(user);
        }

    }
   
   
   
    }
</script>

<style scoped>
a{
    text-decoration: none;
    color:black;
}

</style>