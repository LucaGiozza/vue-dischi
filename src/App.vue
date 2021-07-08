<template>
  <div id="app">

    <Header/>

    <DischiList/>

    
    
  </div>
</template>

<script>

import Header from '@/components/Header.vue';
import DischiList from '@/components/DischiList.vue';


export default {
  name: 'App',
  components: {
    Header,
    DischiList
    
  }
}
</script>

<style lang="scss">

@import '@/style/general.scss' ;

</style>
