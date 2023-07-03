<template>
    <div>
        <nav class="navbar navbar-expand-lg " >
            <div class="container-fluid">
              <a class="navbar-brand" href="#" style="margin-right:30%;">Lithini Skhikhi</a>
              <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarNavDropdown" aria-controls="navbarNavDropdown" aria-expanded="false" aria-label="Toggle navigation">
                <span class="navbar-toggler-icon"></span>
              </button>
              <div class="collapse navbar-collapse" id="navbarNavDropdown">
                <ul class="navbar-nav">
                  <li class="nav-item">
                    <router-link class="nav-link" to="/">Home</router-link>
                  </li>
                  <li class="nav-item">
                    <router-link class="nav-link" to="/about">About</router-link>
                  </li>
                  <li class="nav-item">
                    <router-link class="nav-link" to="/testimonials">Testimonials</router-link>
                  </li>
                  <li class="nav-item">
                    <router-link class="nav-link" to="/Projects">Projects</router-link>
                  </li>
                  <li class="nav-item">
                    <router-link class="nav-link" to="/skills">skills</router-link>
                  </li>
                  <li class="nav-item">
                    <router-link class="nav-link" to="/Contact">contact</router-link>
                  </li>
                 
                </ul>
              </div>
            </div>
          </nav>
    </div>
</template>

<script>
    export default {
        
    }
</script>

<style scoped>
nav{
  background-color: white;
    width: 100vh;
    width: 100%;
    margin-bottom: 3rem;
}
</style>