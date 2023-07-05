<template>
    <div class="mt-5 container">
     <div class="row gap-2">
         <h1 style="padding-top:3rem;">Projects</h1>
         <div class="col-12 col-md-6" v-for="data in Projects" :key="data.id">
<div class="card" style="background-color:black">
             <img :src="data.image" alt="" style="width:6rem;height:6rem;" class="card-img-top">
             <div class="card-body">
             <p>{{data.Name}}</p>
             <a href="id.github">
                <button style="width:3rem,"><ion-icon name="logo-github"></ion-icon></button>
              </a>
              <a href="id.netlify">
                <button>Netlify</button>
              </a>
             <p>{{data.firebase}}</p>
             <p>{{data.netlify}}</p>

        
             <p>{{data.Description}}</p>
            </div>
          </div>
        </div>   
      
    </div>
 </div>
 </template>
 
 <script>
     export default {
         computed:{
            Projects(){
                 return this.$store.state.Projects
             }
         },
         mounted(){
             this.$store.dispatch('fetchProjects')
         }    
     }
     window.addEventListener("scroll", function() {
   //Select your navigation bar
   var nav = document.getElementsByTagName("nav")[0];
   //Change 20 to anything you want like nav.offsetHeight
   if(window.scrollY > 20) {
       nav.style.borderBottom = "5px solid Red";
    } else {
      nav.style.border = "0";
   }
});
 </script>
 
 <style scoped>
 
 </style>