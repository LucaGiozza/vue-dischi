<template>
<header >
    <img class="logo" src="@/assets/spotify.jpg" alt="">
     <select class="scelta-genere">
         <option selected>Scegli il genere</option>
         <option value="1">Rock</option>
         <option value="2">Pop</option>
         <option value="3">Jazz</option>
         <option value="4">Metal</option>
     </select>
</header>

  
</template>

<script>
export default {
    name : 'Header'

}
</script>

<style lang="scss" scoped>

header{
    background-color: black;
    width:100%;
    height:80px;
    display: flex;
    line-height: 80px;
    vertical-align: middle;
    justify-content: space-between;
    align-items: center;
    
    
    

    .logo{
    height:50px;
   
   
    
}

.scelta-genere{
    height: 50%;
    margin-right: 20px;;
    
    
}

}


</style>