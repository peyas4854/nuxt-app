<template>
    <div>
        <nuxt-link to="/">Home </nuxt-link>

        <h2>I am about page hggg  </h2>

        
    </div>
</template>
<script>
export default{
    // layout:'aboutLayout',

    // middleware:'test',
    head(){
        return{
            title:'about',
            meta:[
                {hid:'description',name:'description',content:'about page'}
            ],
        }
    }
}

</script>