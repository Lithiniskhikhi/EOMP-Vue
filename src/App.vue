<template>
 
  <Navbar/>
  <router-view/>
</template>
<script>
import Navbar from '@/components/Navbar.vue';

export default{
  components: {
    Navbar,
  
  }
}
</script>
<style>
body{
  background-color: black;
}

nav {
  padding: 30px;
}

nav a {
  font-weight: bold;
  color: #2c3e50;
}

nav a.router-link-exact-active {
  color: #b9428b;
}
</style>
