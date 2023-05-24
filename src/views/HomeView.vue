<template>
  <div class="home">
    <CardApp :key="item" v-for="item in 10" :imgUser="userimg" :imgCard="card" :title="title" :username="username" :price="price" :cantRoom="rooms" :star="stars"/>
    
  </div>
</template>

<script>
// @ is an alias to /src
import CardApp from '@/components/CardApp.vue'

export default {
  name: 'HomeView',
  components: {
    CardApp
  },
  data(){
    return{
    username: "Angel Quezada",
    userimg: "https://s1.eestatic.com/2020/05/28/actualidad/actualidad_493461652_152691229_1706x960.jpg",
    price : 1500,
    stars : 25,
    title : "Isla mauricio",
    rooms : 5,
    card  : "https://images.unsplash.com/photo-1554132286-24c3f6113a86?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=869&q=80"
    }
    
  }
}
</script>
