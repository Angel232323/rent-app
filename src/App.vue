import CardApp from '@/components/CardApp.vue';
<template>
  <div id="app">
    <div class="navbar-container">
      <div class="navbar-content">
        <router-link to="/"><i class='bx-sm bx bx-home-alt'></i></router-link> 
        <router-link to="/test1"><i class='bx-sm bx bx-heart'></i></router-link>
        <router-link to="/test2"><i class='bx-sm bx bx-location-plus'></i></router-link>
        <router-link to="/test3"><i class='bx-sm bx bx-message-square-detail'></i></router-link>
      </div>
    </div>
    <router-view />
  </div>
</template>
<style lang="less">
* {
  margin: 0px;
  padding: 0px;
  font-family: "Josefin Sans", sans-serif;
}
.navbar-container {
  width: 100%;
  position: fixed;
  bottom: 0;
  z-index: 4000;
  background-color: #fff;

  .navbar-content {
    padding: 15px;
    display: flex;
    justify-content: space-between;
    a{
      color: rgba(95, 100, 111);
      &.router-link-exact-active {
        color: rgba(69, 208, 215);
      }
    }
  }
}
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
}

nav {
  padding: 30px;
}

nav a {
  font-weight: bold;
  color: #2c3e50;
}

 nav a.router-link-exact-active {
  color: red;
}
</style>
