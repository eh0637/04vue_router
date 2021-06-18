<template>

  <!-- <div v-if="pView==true"> 
    <div class="pPop text-center">
      <img v-bind:src="pdata[pNum].image" alt="" class="w-50">
      <p >{{pdata[0].title}}</p>
      <button class="btn btn-primary" @click="pView=false">닫기</button>
    </div>

  </div> -->
  <transition name="fade" class="fadeP">
    <pPop
    :pdata="pdata"
    :pView="pView"
    :pNum="pNum"
    @pClose="pView=false"
    
    
     />
  </transition>


  
  <top-header />
  
  <router-view
   v-bind:pdata="pdata"
   @pOpen="pView=true;pNum=$event"
  ></router-view>

  <bottom-footer />
</template>

<script>
import header from './components/header.vue'
import pdata from './pdata'
import footer from './components/footer.vue'
import pPop from './components/pPop.vue'

export default {

  name:'app',
  components:{
    'top-header':header,
    'bottom-footer':footer,
    pPop
  },
  data(){
    return{
      pdata:pdata,
      pView:false,
      pNum:0
    }
  }
}
</script>

<style>
  .pPop{ 
    position: fixed; z-index: 10; background: #fff; width:80%;
  top:50%; left: 50%;
   transform: translate(-50%, -50%); box-shadow: 0 0 10px rgba(0,0,0,0.5);
   border-radius: 10px;  padding: 20px;
   }
   .fade-enter-from{  opacity: 0;}
   .fade-enter-active{transition: 0.3s;}
   .fade-enter-to{opacity: 1;}

   .fadeP { position: relative; z-index: 100;}
   @media screen and (min-width:900px) {
     .pPop {width: 800px;}
     
   }
</style>