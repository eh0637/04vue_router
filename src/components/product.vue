<template>
  
  <div class="pro">
    <div class="container">
      <h2 class="text-center">PRODUCT</h2>
      <div class="row">
    
            <div class="col-sm-6 col-md-3 " v-for="(item, i) in pdata " :key="i"  @click="$emit('pOpen',pdata[i].id)">
            <div class="hover_box">
              <img :src="pdata[i].image" alt="" class="w-100">
                <div class="hover_bg">
              <div class="contp" v-html="pdata[i].content"></div>
                <div class="contpb">
                {{pdata[i].price}}원
                
                </div>
              </div>
              </div>
             <div class="text-center py-2 productL">
               <div class="ProductTitle">{{pdata[i].title}} </div>
               <div class="ProductCost">{{pdata[i].price}}원 </div>
             </div>



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
.hover_bg{ width: 100%; height: 100%; background:#000; 
      opacity:0;position: absolute; transform:scale(0.6);transition:.3s;
      top: 0; left: 0; padding: 130px 0;}
.hover_box:hover .hover_bg {opacity:0.5; transform:scale(1)}
.contp {color: #fff; text-align: center; font-weight:bold;}
.contpb {color: #fff; text-align: center; font-weight:bold;}
.pro h2{ text-align: center; _margin-bottom: 40px; padding: 40px 0;}
.pro h2::after{
  content: ""; width: 30px; height: 2px; background:#333 ;
  display: block; margin: 10px auto;
}
.pro p { text-align: center; font-weight:bold; margin-bottom: 20px;}
.ptitle { font-weight: bold; padding: 10px 0;}
.ProductTitle{ font-weight: bold; color: #333; font-size: 1rem;}
.ProductCost{font-weight: normal; color: #666; font-size: 0.9rem;}


</style>