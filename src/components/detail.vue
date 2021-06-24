<template>
  <div class="container">

      <router-link to="/company" class="back">뒤로가기</router-link>
      <div >
          <h3 class="stitle">{{bdata[$route.params.idx].title}}</h3>
          <p class="stitles">{{bdata[$route.params.idx].content}}</p>
      </div>
  </div>
</template>

<script>
export default {
    name:'detail',
    props:['bdata']
}
</script>

<style>
    .container{padding:20px}
    .back{font-weight: bold; color: rgb(33, 2, 168); margin-bottom: 20px;}
    .stitle{margin-bottom: 60px; text-align: center;}
    .stitles{padding: 30px; text-align: center; }
    
    
</style>