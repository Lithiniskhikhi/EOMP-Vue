<template>
    <div>
        <nav class="navbar navbar-expand-lg " >
            <div class="container-fluid">
              <a class="navbar-brand" href="#" style="margin-right:30%;"><img src="https://i.postimg.cc/wxFCdn83/Screenshot-2023-07-05-120344.png" id="Lee"></a>
              <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarNavDropdown" aria-controls="navbarNavDropdown" aria-expanded="false" aria-label="Toggle navigation">
                <span class="navbar-toggler-icon"></span>
              </button>
              <div class="collapse navbar-collapse" id="navbarNavDropdown">
                <ul class="navbar-nav">
                  <li class="nav-item">
                    <router-link class="nav-link" to="/" style="color:white">Home</router-link>
                  </li>
                  <li class="nav-item">
                    <router-link class="nav-link" to="/about" style="color:white">About</router-link>
                  </li>
                  <li class="nav-item">
                    <router-link class="nav-link" to="/testimonials" style="color:white">Testimonials</router-link>
                  </li>
                  <li class="nav-item">
                    <router-link class="nav-link" to="/Education" style="color:white">Education</router-link>
                  </li>
                  <li class="nav-item">
                    <router-link class="nav-link" to="/Projects" style="color:white">Projects</router-link>
                  </li>
                  <li class="nav-item">
                    <router-link class="nav-link" to="/skills" style="color:white">skills</router-link>
                  </li>
                  <li class="nav-item">
                    <router-link class="nav-link" to="/Contact" style="color:white">contact</router-link>
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
  background-color: #000;
    width: 100vh;
    width: 100%;
    margin-bottom: 3rem;
}

a:hover {
  background-color: rgb(206, 22, 22);
 border-radius: 30%; 
}
</style>