<template>
  <h2 class="">BOARD</h2>
    <div class="container">
      <table class="table">
  <thead>
    <tr>
      <th scope="col">#</th>
      <th scope="col ">제목</th>
      <th scope="col">작성일</th>

    </tr>
  </thead>
  <tbody>
    <tr v-for="(item,i) in bdata" :key="i" class="">
      <th scope="row">{{bdata[i].idx}}</th>
      <td class="title"><router-link :to='`/detail/${bdata[i].idx}`'>{{bdata[i].title}}</router-link></td>
      <td>{{bdata[i].data}}</td>  
    </tr>
  </tbody>
</table>

    </div>
</template>


<script>
export default {
    name:'company',
    props:['bdata']
  
    
}
</script>

<style>
table{text-align: center; color: #333;}
.title{text-align: left; }
.title:hover{background: #efefef; font-weight: bold;}
h2{text-align: center;}
</style>