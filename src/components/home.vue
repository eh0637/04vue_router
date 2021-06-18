<template>

<swiper :pagination="true" class="mySwiper">
  <swiper-slide><img src="images/s1.jpg" alt=""></swiper-slide>
  <swiper-slide><img src="images/s2.jpg" alt=""></swiper-slide>
  </swiper>
  <div class="best">
    <div class="container">
      <h2>BEST</h2>
      <p>스파오 best 상품</p>
      <div class="row">
        <div class="col-sm-6 col-md-3" v-for="(item, i) in 4 " :key="i">
          <img :src="pdata[i].image" alt="" class="w-100">
          <div @click="$emit('pOpen',pdata[i].id)">{{pdata[i].title}} </div>
        </div>
      </div>

      <div class="btn btn-primary ">
        <router-link to="/product">more</router-link>
      </div>
    </div>
  </div>

</template>

<script>
import { Swiper, SwiperSlide } from 'swiper/vue';
import "swiper/components/pagination/pagination.min.css"


// Import Swiper styles
import 'swiper/swiper.scss';
import SwiperCore, {
  Pagination
} from 'swiper/core';

// install Swiper modules
SwiperCore.use([Pagination]);


export default {
    props:['pdata'],
    components: {
    Swiper,
    SwiperSlide,
  },
  data() {
    return {
        
        
    };
  },
  methods: {
    
  }

}
</script>

<style>
.swiper-container {
  width: 100%;
  height: 100%;
}

.swiper-slide {
  text-align: center;
  font-size: 18px;
  background: #fff;

  /* Center slide text vertically */
  display: -webkit-box;
  display: -ms-flexbox;
  display: -webkit-flex;
  display: flex;
  -webkit-box-pack: center;
  -ms-flex-pack: center;
  -webkit-justify-content: center;
  justify-content: center;
  -webkit-box-align: center;
  -ms-flex-align: center;
  -webkit-align-items: center;
  align-items: center;
}

.swiper-slide img {
  display: block;
  width: 100%;
  height: 100%;
  object-fit: cover;
}

.best h2{ text-align: center;}
.best h2::after{
  content: ""; width: 30px; height: 2px; background:#333 ;
  display: block; margin: 10px auto;
}
.best p { text-align: center; font-weight:bold; margin-bottom: 20px;}

.mySwiper{margin-bottom: 40px;}


</style>