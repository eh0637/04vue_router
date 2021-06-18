<template>
  <h1>logo</h1>
  <nav class="navbar navbar-expand-lg navbar-light bg-light">
  <a class="navbar-brand" href="/">LOGO</a>
  <button class="navbar-toggler" type="button" data-toggle="collapse" data-target="#navbarNav" aria-controls="navbarNav" aria-expanded="false" aria-label="Toggle navigation">
    <span class="navbar-toggler-icon"></span>
  </button>
  <div class="collapse navbar-collapse" id="navbarNav">
    <ul class="navbar-nav ml-auto menu">
      <li class="nav-item  " v-for="(a, i) in menu" :key="i">
        <router-link :to="menu[i].link" class="nav-link">{{menu[i].title}}</router-link>
      </li>
      <!-- <li class="nav-item">
        <a class="nav-link" href="#">Features</a>
      </li>
      <li class="nav-item">
        <a class="nav-link" href="#">Pricing</a>
      </li> -->
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
                {title:'home',link:'/'},
                {title:'company',link:'/company'},
                {title:'product',link:'/product'}
            ]
        }
    }

}
</script>

<style>
li.nav-item { width: 100px;}  
li.nav-item a{ text-align: center; line-height: 40px;}
a:hover{ text-decoration: none;}
a{display: block;}
</style>