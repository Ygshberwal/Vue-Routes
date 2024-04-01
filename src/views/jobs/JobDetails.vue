<template>
    <h1>Jobs Details Page</h1>
    <p>This job has id: {{ id }}  </p>
</template>

<script>
export default{
    props:['id','title'],
    // data(){
    //     return{
    //     id:this.$route.params.id,
    //     }      
    // }
    
}
</script>
<style>
</style>