<template>
  <div>
      <v-toolbar color="indigo" dark>
      <v-app-bar-nav-icon></v-app-bar-nav-icon>
      <v-toolbar-title>Nuxt Application Api call </v-toolbar-title>
      <v-spacer></v-spacer>
        <v-toolbar-items>

          
            <v-btn text>
                <N-link  to="/" text >home</N-link>
            </v-btn> 
           <v-btn text>
                <N-link  to="/user" text >user</N-link>
            </v-btn> 
           <v-btn text>
                <N-link  to="/" text >todo</N-link>
              
            </v-btn> 
            <v-btn text>
                
            <N-link  to="/about" text >About</N-link>
            
            </v-btn>
            <v-btn text>

            <N-link  to="/blog" text >Blog</N-link>
            
            </v-btn>
           
        </v-toolbar-items>
    </v-toolbar> 
  </div>
</template>

<script>

</script>

<style  scoped>
a{
    
    color:white!important;
    text-decoration: none;
}

</style>