<template>
<v-app>
  <v-content>
    <navbar/>
    <v-container >
        <div>
            <nuxt/>
          </div>
    </v-container>
    <appfooter/>
  </v-content>
</v-app>
</template>
<script>
import navbar from "../components/navbar.vue";
import appfooter from "../components/appfooter.vue";
export default {
  components:{
    navbar,
    appfooter
  }
  
}
</script>
<style scoped>
a{
  text-decoration: none;
  color:white!important;
}
</style>