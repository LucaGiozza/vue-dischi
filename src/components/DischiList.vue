<template>
<section class="container" >
    <div  class="row colonne" v-if="!semaforo">
          <div  v-for="dischi in dischiArray" :key="dischi.poster" class="col-2 immagini  "> 
           
                 <Musica :details="dischi" />
              
             
        
            
        </div> 
        

    </div>

   <img class="orso" v-else src="@/assets/load.jpg" alt="">

</section>
  
</template>

<script>

import axios from 'axios';
import Musica from '@/components/Musica.vue'

export default {
    name: 'DischiList',

    components :{
        Musica
    },

    data(){
        return{
            apiURL : 'https://flynn.boolean.careers/exercises/api/array/music',
            dischiArray : '',
            semaforo: true
        }


    },
    created(){
        this.getDischi();

    },
    methods:{
        getDischi(){
            axios
            .get(this.apiURL)
            .then(risposta =>{
                
                this.dischiArray = risposta.data.response;
                console.log(this.dischiArray);
                this.semaforo = false;

            })
            .catch(error =>{
                console.log(error);
            })

        }
    }

}
</script>

<style lang="scss" scoped>
.container{
   text-align: center;
   
    margin-top:20px;
    img{
        height: 150px;
        
    

    }
    .colonne{
       justify-content: space-around;
        
    }
    .immagini{
        width:20%;
        
    }
    .orso{
        height:600px;
    }

}
   
        

</style>