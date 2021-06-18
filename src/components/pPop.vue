<template>
    <div v-if="pView==true"> 
    <div class="pPop text-center">
      <img v-bind:src="pdata[pNum].image" alt="" class="w-50">
      <p >{{pdata[0].title}}</p>
      <button class="btn btn-primary" @click="$emit('pClose')" >닫기</button>
    </div>  

  </div>
</template>

<script>
export default {
    name:'pPop',
    props:['pView','pdata','pNum']

}
</script>

<style>



</style>