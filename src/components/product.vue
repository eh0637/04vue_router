<template>
  
  <div class="pro">
    <div class="container">
      <h2 class="text-center">product</h2>
      <div class="row">
    
            <div class="col-sm-6 col-md-3 " v-for="(item, i) in pdata " :key="i">
            <div class="hover_box">
              <img :src="pdata[i].image" alt="" class="w-100">
                <div class="hover_bg">
              <div class="contp" v-html="pdata[i].content"></div>
                <div class="contpb">
                {{pdata[i].price}}원
                
                </div>
              </div>
              </div>
             <div @click="$emit('pOpen',pdata[i].id)">{{pdata[i].title}} </div>



          </div>
          
    
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name:'product',
  props:['pdata'],

}
</script>

<style>
.hover_box {position: relative; }
.hover_bg{ width: 90%; height: 90%; background:#000; padding: 130px 0;
      opacity:0;position: absolute; transform:scale(0.6);transition:.3s;
      top: 0; left: 15px; _border-radius: 10px}
.hover_box img:hover .hover_bg {opacity:0.5; transform:scale(1)}
.contp {color: #fff; text-align: center; font-weight:bold;}
.contpb {color: #fff; text-align: center; font-weight:bold;}
.pro h2{ text-align: center; _margin-bottom: 40px; padding: 40px 0;}
.pro h2::after{
  content: ""; width: 30px; height: 2px; background:#333 ;
  display: block; margin: 10px auto;
}
.pro p { text-align: center; font-weight:bold; margin-bottom: 20px;}
.ptitle { font-weight: bold; padding: 10px 0;}

</style>