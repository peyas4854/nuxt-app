<template>
<div>
<nuxt/>
<v-footer>
    <v-spacer></v-spacer>
    <div>&copy; {{ new Date().getFullYear() }}</div>
  </v-footer>
</div>
</template>
<script>
export default {
    data(){
        return{
            title:'I am layout for about'
        }
    }

}
</script>

