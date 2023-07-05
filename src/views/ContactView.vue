<template>
    
<!--Section: Contact v.2-->
<section class="mb-4" style="margin-inline: 2rem;">

  <!--Section heading-->
  <h2 class="h1-responsive font-weight-bold text-center my-4">Contact Me !</h2>
  <!--Section description-->
  <p class="text-center w-responsive mx-auto mb-5"></p>
     

  <div class="row">

      <!--Grid column-->
      <div class="col-md-9 mb-md-0 mb-5">
          <form id="contact-form" name="contact-form" action="mail.php" method="POST">

              <!--Grid row-->
              <div class="row">

                  <!--Grid column-->
                  <div class="col-md-6">
                      <div class="md-form mb-0">
                        <label for="name" class="">Your name</label>
                          <input type="text" id="name" name="name" class="form-control">
                         
                      </div>
                  </div>
                  <!--Grid column-->

                  <!--Grid column-->
                  <div class="col-md-6">
                      <div class="md-form mb-0">
                        <label for="email" class="">Your email</label>
                          <input type="text" id="email" name="email" class="form-control">
                          
                      </div>
                  </div>
                  <!--Grid column-->

              </div>
              <!--Grid row-->

              <!--Grid row-->
              <div class="row">
                  <div class="col-md-12">
                      <div class="md-form mb-0">
                        <label for="subject" class="">Subject</label>
                          <input type="text" id="subject" name="subject" class="form-control">
                          
                      </div>
                  </div>
              </div>
              <!--Grid row-->

              <!--Grid row-->
              <div class="row">

                  <!--Grid column-->
                  <div class="col-md-12">

                      <div class="md-form">
                        <label for="message">Your message</label>
                          <textarea type="text" id="message" name="message" rows="2" class="form-control md-textarea"></textarea>
                        <br>
                      </div>

                  </div>
              </div>
              <!--Grid row-->

          </form>

          <div class="text-center text-md-left">
              <a class="btn btn-primary" onclick="document.getElementById('contact-form').submit();" id="send"><ion-icon name="mail-open-outline" ></ion-icon ></a>
          </div>
          <div class="status"></div>
      </div>
      <!--Grid column-->

      <!--Grid column-->
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
      <!--Grid column-->

  </div>

</section>
<!--Section: Contact v.2-->
  
</template>

<script>
    export default {
        
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

<style src="../assets/css/styles.css">


</style>
