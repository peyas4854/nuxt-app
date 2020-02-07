<template>
  <div>
    <h1 class="text-uppercase" >This is erorr page </h1>
    <h3 class="display-1">{{ error.statusCode }}</h3>
    
  </div>
</template>

<script>
export default {
   layout:'errorLayout',
    props: {
    error: {
      type: Object,
      default: null
    }
  }
   

}
</script>

