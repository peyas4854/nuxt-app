<template>
    <div>
       
        <h2>I am about page hggg  </h2>
    </div>
</template>
<script>
export default{
    // layout:'aboutLayout',

    // middleware:'test',
    head(){
        return{
            title:'About Page ',
            meta:[
                {hid:'description',
                name:'description',
                content:'Nuxt js Toodo Application'}
            ],
        }
    }
}

</script>