<template>
  <div>
      <h2> I am Dynamic blog page = {{ route.blog }} </h2>

     
     </div>   
</template>

<script>
export default {

  data(){
    return{
      route:this.$route.params,
    }
  },
  created(){
    console.log(this.$route.params);
  }

}
</script>

<style>

</style>