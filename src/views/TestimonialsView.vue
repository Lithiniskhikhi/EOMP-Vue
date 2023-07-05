<template>
    <div class="mt-5 container" >
     <div class="row ">
         <h2 style="padding-top:3rem;">Testimonials</h2>
         <div class="col-12 col-md-6" v-for="data in Testimonials" :key="data.id">
<div class="card" style="background-color:#050505">
             <img :src="data.image" alt="" style="width:20rem;height:15rem;" class="card-img-top">
             <div class="card-body" style="width:15rem;height:25rem;">
             <p>{{data.Name}}</p>
             <p>{{data.relationship}}</p>
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
            Testimonials(){
                 return this.$store.state.Testimonials
             }
         },
         mounted(){
             this.$store.dispatch('fetchTestimonials')
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