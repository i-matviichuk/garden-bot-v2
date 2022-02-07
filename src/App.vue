<template>
  <div id="app">
    <div class="header">
      <!-- header -->
    </div>
    <div class="body-box">
      <div id="nav" class="sidebar">
        <Sidebar/>
      </div>
      <div class="content-box">
        <router-view/>
      </div>
    </div>
    <div class="footer">
      <!-- footer -->
    </div>
  </div>
</template>

<script>
import Sidebar from '@/components/Sidebar.vue'
export default {
  components: {
    Sidebar
  }
}
</script>

<style>
  body {
    height: 100%;
    margin: 0;
    overflow: hidden;
    display: flex;
    flex-direction: column;
  }
  .body-box {
    flex-grow: 1;
    display: flex;
  }
  .content-box {
    overflow: scroll;
    height: 100vh;
    flex-grow: 1;
    display: flex;
    flex-direction: column;
  }

  #app {
    font-family: Avenir, Helvetica, Arial, sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    /*text-align: center;*/
    color: #2c3e50;
  }

  #nav {
    padding: 30px 10px 10px 30px;
  }

  #nav a {
    font-weight: bold;
    color: #2c3e50;
    text-decoration: none;
  }

  #nav a.router-link-exact-active {
    color: #42b983;
  }
</style>
