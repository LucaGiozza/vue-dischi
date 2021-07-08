<template>
<div class="container">
    <img  class="fotografie" :src="details.poster" :alt="details.title">
    <h3 class="titolo">{{details.title}}</h3>
    <p class="autore">{{details.author}}</p>
</div>
  
</template>

<script>
export default {
    name: 'Musica',
    props:["details"]

}
</script>

<style lang="scss" >
.container{
    background-color:rgba(0, 0, 0, 0.8);
    padding:30px;
    

}
.fotografie{
    height: 180px;
    margin-top:40px;
    width:100%;
   
    

    

    
    
    
    
}
.titolo{
    font-size: 14px;
    margin-top:10px;
    color:white;
}
.autore{
    font-size: 12px;
    color:white;
}

</style>