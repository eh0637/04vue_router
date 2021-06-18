<template>
  <top-header />
  
  <router-view v-bind:pdata="pdata"></router-view>

  <bottom-footer />
</template>+

<script>
import header from './components/header.vue'
import pdata from './pdata'
import footer from './components/footer.vue'

export default {

  name:'app',
  components:{
    'top-header':header,
    'bottom-footer':footer,
  },
  data(){
    return{
      pdata:pdata,
    }
  }
}
</script>

<style>

</style>