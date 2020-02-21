<template>
  <v-parallax src="https://cdn.vuetifyjs.com/images/parallax/material.jpg">
<div>
     <v-card class="text-center" >
        <v-list-item three-line>
        <v-list-item-content>
            <!-- <div class="overline mb-4">User name </div> -->
            <v-list-item-title class="headline mb-1">
                  {{ users.name }}  
            </v-list-item-title>
            <v-list-item-subtitle></v-list-item-subtitle>
             <v-list-item>
            <v-list-item-content>
                <v-list-item-title v-if="users.email == users.email "><b>Email</b> :    {{ users.email }} </v-list-item-title>
                <v-list-item-title v-if="users.website == users.website "><b>Website</b> :   {{ users.website }} </v-list-item-title>
                <v-list-item-title v-if="users.phone == users.phone "><b>Phone</b> :   {{ users.phone }} </v-list-item-title>
            </v-list-item-content>
    </v-list-item>
        </v-list-item-content>
        </v-list-item>
        <v-card-actions>
        <v-btn text  color="info" >
           <N-link  to="/user" >  Back </N-link>
           <v-icon color="green"> mdi- </v-icon>
            </v-btn>
        </v-card-actions>
    </v-card>
</div>
</v-parallax>
</template>
<script>
export default {
     head(){
        return{
            title:this.users.name,
            meta:[
                {hid:'description',
                name:'description',
                content:'Nuxt js Toodo Application'}
            ],
        }
    },
     validate ({ params }) {
    // Must be a number
    return /^\d+$/.test(params.user)
  },
    data(){
     return{
         id:'',
         users:'',
      }
    },
    created(){
     this.id = this.$route.params.user;
     this.fetchuser(this.id)   
  },
    methods:{
        async fetchuser(id){
            const user = await this.$axios.$get(`https://jsonplaceholder.typicode.com/users/${this.id}`)
            this.users = user;
           
        }
    }       
}        
</script>
<style scoped>
a{
    
   
    text-decoration: none;
}
</style>
