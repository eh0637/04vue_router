<template>
  <div>
    <a href="/"><img src="images/logo_spao_b.jpg" alt="" class="logo"></a>
  </div>
  <nav class="navbar navbar-expand-lg navbar-light ">

  <button class="navbar-toggler ml-auto" type="button" data-toggle="collapse" data-target="#navbarNavDropdown" aria-controls="navbarNavDropdown" aria-expanded="false" aria-label="Toggle navigation">
    <span class="navbar-toggler-icon"></span>
  </button>
  <div class="collapse navbar-collapse" id="navbarNavDropdown">
    <ul class="navbar-nav ml-auto mr-auto">
      <li class="nav-item" v-for="(a, i) in menu" :key="i" >
        <router-link :to="menu[i].link">{{menu[i].title}}</router-link>
      </li>

    </ul>
  </div>
</nav>
  <!-- <ul class="clearfix menu">
      <li v-for="(a, i) in menu" :key="i">
          <router-link :to="menu[i].link">{{menu[i].title}}</router-link>
      </li>
  </ul> -->



</template>

<script>
export default {
    name:'header',
        data(){
        return{
          
            menu:[
                {title:'HOME',link:'/'},
                {title:'PRODUCT',link:'/product'},
                {title:'BOARD',link:'/company'},

            ]
        }
    },
    methods:{
      close:function(){
        document.getElementById("navbarNav").classList.remove("show")
      }
    }

}
</script>

<style>
h1{font-weight:bold; padding: 20px 0 ;}
li.nav-item { width: 100px;}  
li.nav-item a{ text-align: center; line-height: 40px;}
a:hover{ text-decoration: none;}
a{display: block;}
.logo{    margin: 0 auto;
    display: block;
    padding: 30px 0;}
</style>