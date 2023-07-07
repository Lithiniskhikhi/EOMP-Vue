<template>
   

 

<h1 class="testimonials">TESTIMONIALS</h1>
  <div class="container d-flex justify-content-center" >
    <div id="testcard" class="card mb-3">
  <div class="row g-0 p-0" id="tcard"
            v-for="data in Testimonials"
            :key="data.id">
    <div class="col-md-4">
      <img :src="data.image" class="img-fluid rounded-start" :alt="data.name">
    </div>
    <div class="col-md-8">
      <div class="card-body testt h-100">
        <h5 class="card-title text-white">{{data.Name}}</h5>
        <p class="card-text">{{data.relationship}}</p>
        <p class="card-text">{{data.Description}}</p>
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
 #tcard{
    border-radius: 4px;
    box-shadow: 0 6px 10px rgba(0,0,0,.08), 0 0 6px rgba(0,0,0,.05);
      transition: .3s transform cubic-bezier(.155,1.105,.295,1.12),.3s box-shadow,.3s -webkit-transform cubic-bezier(.155,1.105,.295,1.12);
  padding: 14px 80px 18px 36px;
  cursor: pointer;
}
#tcard:hover{
     transform: scale(1.05);
  box-shadow: 0 10px 20px rgba(0,0,0,.12), 0 4px 8px rgba(0,0,0,.06);
}

.testt{
    display: flex;
    justify-content: center;
    align-items: center;
    flex-direction: column;
    text-align: center;
    /* padding-top: 3rem; */
  }

  .testimonials {
    margin-top: 4rem;
    margin-bottom: 2rem;
  }
  #testcard {
    width: 80%;
    border: none;
    background-color: black;
  }
  
  #tcard {
    margin-bottom: 1rem;
  }
  
  
 </style>