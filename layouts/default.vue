<template>
<v-app>
  <v-content
    
  >

    <v-toolbar color="indigo" dark>
      <v-app-bar-nav-icon></v-app-bar-nav-icon>
      
      <v-toolbar-title>Title</v-toolbar-title>
      <v-spacer></v-spacer>
        <v-toolbar-items>
          <!-- <nuxt-link to="/" >weather App</nuxt-link> -->
          <v-btn text>
                <N-link  to="/" text >weather App</N-link>
              
              </v-btn> 
              <v-btn text>
                <N-link  to="/about" text >About</N-link>
              
              </v-btn>
        </v-toolbar-items>
    </v-toolbar>
    <v-container>

    <h1 class="text-center display-1">Employee Data </h1>
   
      <v-card color="blue" dark >
      <v-card-title text-center>
       Employee Record 
      </v-card-title>
    </v-card>
    <v-text-field class="mt-5"
            label="Enter city Name " solo
          >
          
    </v-text-field>
    </v-container>

  <div>
     <nuxt/>
  </div>
  </v-content>
</v-app>
</template>
<script>
export default {
  
}
</script>
<style scoped>
a{
  text-decoration: none;
  color:white!important;
}
</style>