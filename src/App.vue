<template>
  <Sidebar />
  <div class="mainSection" :style="{ 'margin-left': sidebarWidth }">
      <router-view/>
  </div>
</template>

<script>
  import Sidebar from './components/sidebar/Sidebar.vue'
  import { sidebarWidth } from './components/sidebar/state'
  export default {
    components: { Sidebar },
    setup() {
      return { sidebarWidth }
    }
  }
</script>

<style>
#app {
  font-family: Poppins, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
}

#nav {
  padding: 30px;
}

#nav a {
  font-weight: bold;
  color: #2c3e50;
}

#nav a.router-link-exact-active {
  color: #42b983;
}

.mainSection {
  transition: 0.3s ease;
}
</style>
