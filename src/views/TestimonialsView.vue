<template>
    <div class="mt-5 container">
     <div class="row gap-2">
         <h1 style="padding-top:3rem;">Testimonials</h1>
         <div class="col-12 col-md-6" v-for="data in Testimonials" :key="data.id">
<div class="card" style="background-color:black">
             <img :src="data.image" alt="" style="width:6rem;height:6rem;" class="card-img-top">
             <div class="card-body">
             <p>{{data.Name}}</p>
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
 </script>
 
 <style scoped>
 
 </style>