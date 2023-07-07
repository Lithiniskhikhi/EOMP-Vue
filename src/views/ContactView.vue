<template>
    
<section class="mb-4" style="margin-inline: 2rem;">

  <h2 class="h1-responsive font-weight-bold text-center my-4">Contact Me !</h2>
  <p class="text-center w-responsive mx-auto mb-5"></p>
     

  <div class="row">

      <div class="col-md-9 mb-md-0 mb-5">
          <form id="contact-form" name="contact-form" action="https://formspree.io/f/mwkdkkkw"
          method="POST" required autocomplete="off" >

              <div class="row">

                  <div class="col-md-6">
                      <div class="md-form mb-0">
                        <label for="name" class="">Your name</label>
                          <input type="text" id="name" name="name" class="form-control" required autocomplete="off">
                         
                      </div>
                  </div>
               

                 
                  <div class="col-md-6">
                      <div class="md-form mb-0">
                        <label for="email" class="">Your email</label>
                          <input type="text" id="email" name="email" class="form-control" required autocomplete="off">
                          
                      </div>
                  </div>
                 

              </div>
           
              <div class="row">
                  <div class="col-md-12">
                      <div class="md-form mb-0">
                        <label for="subject" class="">Subject</label>
                          <input type="text" id="subject" name="subject" class="form-control" required >
                          
                      </div>
                  </div>
              </div>
            
              <div class="row">

                  
                  <div class="col-md-12">

                      <div class="md-form">
                        <label for="message">Your message</label>
                          <textarea type="text" id="message" name="message" rows="2" class="form-control md-textarea" required></textarea>
                        <br>
                      </div>

                  </div>
              </div>
              

          </form>

          <div class="text-center text-md-left">
              <a class="btn btn-primary" onclick="document.getElementById('contact-form').submit();" id="send" action="https://formspree.io/f/mwkdkkkw"
              method="POST"><ion-icon name="mail-open-outline" ></ion-icon ></a>
          </div>
          <div class="status"></div>
      </div>
     
      <div class="col-md-3 text-center">
          <ul class="list-unstyled mb-0">
              <li><i class="fas fa-map-marker-alt fa-2x"></i>
                  <p>Cape Town, Western cape, RSA</p>
              </li>

              <li><i class="fas fa-phone mt-4 fa-2x"></i>
                  <p>079 819 1831</p>
              </li>

              <li><i class="fas fa-envelope mt-4 fa-2x"></i>
                  <p>lithiniskhikhi9@gmail.com</p>
              </li>
          </ul>
      </div>
     

  </div>

</section>

  
</template>

<script>
    export default {
        
    }
    window.addEventListener("scroll", function() {
   var nav = document.getElementsByTagName("nav")[0];
   if(window.scrollY > 20) {
       nav.style.borderBottom = "5px solid Red";
    } else {
      nav.style.border = "0";
   }
});



</script>

<style src="../assets/css/styles.css">


</style>
