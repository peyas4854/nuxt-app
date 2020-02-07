<template>
<div>
  <v-card
    color="grey lighten-4"
    flat
    height="200px"
    tile
  >
    <v-toolbar dense>
      <v-app-bar-nav-icon></v-app-bar-nav-icon>
      <v-toolbar-title>Title</v-toolbar-title>
      <v-spacer></v-spacer>
       <v-toolbar-items class="hidden-sm-snd-down">
         <v-btn text >
        <nLink to="/">Home</nLink>
      </v-btn>
       <v-btn text>
        <nLink to="/about">About</nLink>
      </v-btn >
       <v-btn text >
        <nLink to="/inspire">Page 1</nLink>
      </v-btn>

      <v-btn text >
        <nLink to="/blog">Blog</nLink>
      </v-btn>
      

       </v-toolbar-items>
    </v-toolbar>
    <div>
        <nuxt/>
    </div>
    
  </v-card>
  
  </div>
</template>

<script>
export default {
  data () {
    return {
      title: 'I am default Layout!'
    }
  }
}
</script>
