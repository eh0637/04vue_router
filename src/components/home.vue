<template>

<swiper :pagination="true" :autoplay="true" class="mySwiper">
  <swiper-slide><img src="images/slider1.jpg" alt=""></swiper-slide>
  <swiper-slide><img src="images/slider2.jpg" alt=""></swiper-slide>
  <swiper-slide><img src="images/slider3.jpg" alt=""></swiper-slide>
  <swiper-slide><img src="images/slider4.jpg" alt=""></swiper-slide>
  <swiper-slide><img src="images/slider5.jpg" alt=""></swiper-slide>

  </swiper>



  <div class="container">
    <div class="tab">
      <ul class="clearfix">

        <li @click="current = 0" :class="{active:current == 0}"><a href="#!">BEST</a></li>
        <li @click="current = 1" :class="{active:current == 1}"><a href="#!">NEW</a></li>
          
      </ul>
    </div>

    <div>
      <div v-if="current==0">
      <swiper :slidesPerView="4" :spaceBetween="30" :autoplay="false"    :pagination="{
      type: 'progressbar',
    }" :loop="true"
    :breakpoints='{
  "0": {
    "slidesPerView": 2,
    "spaceBetween": 20
  },
  "800": {
    "slidesPerView": 3,
    "spaceBetween": 40
  },
  "1024": {
    "slidesPerView": 5,
    "spaceBetween": 30
  }
}'
     class="mySwiper" >
      <swiper-slide><img src="images/p1.jpg" alt=""> </swiper-slide>
      <swiper-slide><img src="images/p2.jpg" alt=""></swiper-slide>
      <swiper-slide><img src="images/p3.jpg" alt=""></swiper-slide>
      <swiper-slide><img src="images/p4.jpg" alt=""></swiper-slide>
      <swiper-slide><img src="images/p5.jpg" alt=""></swiper-slide>
      </swiper>
      <div class="btn mb-4"><router-link to="/product">more</router-link></div>
      </div>
      <div v-if="current==1">
       <swiper :slidesPerView="4" :spaceBetween="30" :autoplay="true" :pagination="{
      type: 'progressbar',
    }" :loop="true" 
           :breakpoints='{
  "0": {
    "slidesPerView": 2,
    "spaceBetween": 20
  },
  "800": {
    "slidesPerView": 3,
    "spaceBetween": 40
  },
  "1024": {
    "slidesPerView": 5,
    "spaceBetween": 30
  }
}'
       class="mySwiper">
      <swiper-slide><img src="images/n1.jpg" alt=""></swiper-slide>
      <swiper-slide><img src="images/n2.jpg" alt=""></swiper-slide>
      <swiper-slide><img src="images/n3.jpg" alt=""></swiper-slide>
      <swiper-slide><img src="images/n4.jpg" alt=""></swiper-slide>
      <swiper-slide><img src="images/n5.jpg" alt=""></swiper-slide>
      </swiper>
      <div class="btn mb-4"><router-link to="/product">more</router-link></div>
      </div>
    </div>
  <div class="bannerSlider">
    <swiper class="mySwiper" :navigation="true">
      <swiper-slide ><img src="images/banner1.jpg" alt=""></swiper-slide>
      <swiper-slide><img src="images/banner2.jpg" alt=""></swiper-slide>
      <swiper-slide><img src="images/banner3.jpg" alt=""></swiper-slide>
      <swiper-slide><img src="images/banner4.jpg" alt=""></swiper-slide>
  </swiper>
  </div>  
  <div class="snsSlide">
    <h4 class="mb-5">#WIDTH SPAO</h4>  
      <swiper :slidesPerView="5" :spaceBetween="30"  :loop="true"   
          :breakpoints='{
  "0": {
    "slidesPerView": 3,
    "spaceBetween": 20
  },
  "800": {
    "slidesPerView": 4,
    "spaceBetween": 40
  },
  "1024": {
    "slidesPerView": 5,
    "spaceBetween": 30
  }
}'
       class="mySwiper">
      <swiper-slide><img src="images/sns1.jpg" alt=""></swiper-slide>
      <swiper-slide><img src="images/sns2.jpg" alt=""></swiper-slide>
      <swiper-slide><img src="images/sns3.jpg" alt=""></swiper-slide>
      <swiper-slide><img src="images/sns4.jpg" alt=""></swiper-slide>
      <swiper-slide><img src="images/sns5.jpg" alt=""></swiper-slide>
      <swiper-slide><img src="images/sns6.jpg" alt=""></swiper-slide>
      <swiper-slide><img src="images/sns7.jpg" alt=""></swiper-slide>
  </swiper>
    
  </div>


  <div class="container"></div>


  </div>
  <div class="container bannerS">
    <div class="row mb-5">
          <div class="col-md-8 order-1 order-md-1 mb-5 mb-md-0">
            <img src="images/card1.jpg" alt="" class="img-fluid box_S">
          </div>
          <div class="col-md-4 col-sm-12 d-flex flex-column justify-content-center order-2 order-md-2 ">
            <div class="bannerText ml-auto mr-auto ml-md-0  text-center text-md-left">
              <h4>기분좋은 쾌적한 일상</h4>
              <p>이물감이 없고 밀착감이 뛰어나며 <br>겉으로 이너 라인이 드러나지 않아 깔끔합니다.</p>
            </div>

          </div>
    
        </div>
            <div class="row mb-5 ">
            <div class="col-md-4 col-sm-12 d-flex flex-column justify-content-center order-4 order-md-3">
            <div class="bannerText ml-auto mr-auto ml-md-0  text-center text-md-left">
              <h4>가벼운 청바지가 주는 자유로움</h4>
              <p>여름에 적합한 얇은 소재로 만들어져 <br>더욱 가볍고 쾌적한 착용이 가능합니다. </p>
            </div>

          </div>
          <div class="col-md-8 col-sm-12 mb-5 mb-md-0  order-3 order-md-4">
            <img src="images/card2.jpg" alt="" class="img-fluid box_S">
          </div>

    
        </div>
            <div class="row mb-5">
          <div class="col-md-8 col-sm-12 mb-5 mb-md-0  order-5 order-md-5">
            <img src="images/card3.jpg" alt="" class="img-fluid box_S">
          </div>
          <div class="col-md-4  col-sm-12 d-flex flex-column justify-content-center  order-6 order-md-6">
            <div class="bannerText ml-auto mr-auto ml-md-0  text-center text-md-left">
              <h4>햇살 아래서 더 빛나는 청량감</h4>
              <p>여름 내내 지루하지 않을 <br> 당신만의 셋업을 완성하세요.</p>
            </div>

          </div>
    
        </div>

  </div>




</template>

<script>
import { Swiper, SwiperSlide } from 'swiper/vue';
import 'swiper/swiper.scss';
import "swiper/components/pagination/pagination.min.css"
import "swiper/components/navigation/navigation.min.css"

import '../../public/css/style.css';


// Import Swiper styles

import SwiperCore, {
  Pagination,Autoplay,Navigation
} from 'swiper/core';

// install Swiper modules
SwiperCore.use([ Pagination, Autoplay,Navigation]);




export default {
    props:['pdata'],
    components: {
    Swiper,
    SwiperSlide,


  },
  data() {
    
    return {

      current:0,
        
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
.btnMore {display: flex;
    justify-content: center;
    align-items: center;}
    .btnMore a:hover{ border-bottom:1px solid #333 ; }
.tab li {float: left; width: 100px;} 
.tab li a {display: block; text-align: center; color: #666; font-weight: normal;}
.tab ul{    display: flex;
    justify-content: center;}
.bannerS h4{font-weight: bold;}
.tab li.active a{font-weight: bold; color: #333;} 
.btn{    display: flex;
    justify-content: center;
    align-items: center; font-weight: bold; 
    }
    .btn a {color: #666; display: block; transition: 0.3s;}
    .btn a:hover{color: #333; text-shadow: 3px 3px 3px rgba(0,0,0,0.2);}
  
  .swiper-pagination-progressbar .swiper-pagination-progressbar-fill {
    background: #333 !important;
    }
.swiper-pagination-progressbar.swiper-pagination-progressbar-opposite  {
    width: 100%;
    height: 4px;
    left: 0;
    bottom: 0 !important;
}
.box_S{box-shadow: 9px 10px 5px rgba(0,0,0,0.1);}
.snsSlide h4 {font-weight: bold;}

</style>