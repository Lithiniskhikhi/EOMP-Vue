<template>
 
  <Navbar/>
  <router-view/>
 <Footer/>
</template>
<script>
import Navbar from '@/components/Navbar.vue';
import Footer from '@/components/Footer.vue';

export default{
  components: {
    Navbar,
  Footer
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
