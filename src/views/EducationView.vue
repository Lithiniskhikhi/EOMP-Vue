<template>
    <div>
     <h1>-Education- </h1> 
    </div>
<br>
        <!-- <div class="container left" v-for="data in Education" :key="data.id" style="width:25rem;">
          <div class="content">
            <h2>2017</h2>
            <img :src="data.image" alt="" >
                    <p style="color:black">{{data.title}}</p>
                    <p style="color:black">{{data.Timeline}}</p>
                    <p style="color:black">{{ data.Description }}</p>
          </div>
        </div>

        <br> -->
        <br>

        <div class="d-flex justify-content-center align-items-center flex-column ">
          <div class="card" v-for="data in Education" :key="data.id" style="width: 18rem; margin-bottom: 4rem;">
            <img :src="data.image" alt="" >
            <div class="card-body">
              <p style="color:black">{{data.title}}</p>
                      <p style="color:black">{{data.Timeline}}</p>
                      <p style="color:black">{{ data.Description }}</p>
            </div>
          </div>
        </div>
<br>




        <div class="card text-center" style="background-color: black;">
          <div class="card-header" style="color:white">
            MY CV
          </div>
          <div class="card-body">
            <h5 class="card-title" style="color:white">Download my cv</h5>
            <p class="card-text"></p>

            <a href="https://drive.google.com/uc?export=download&id=1ReUg5Fd7RYZmtZLE7QDpoWVUwmzKzt75" class="btn btn-primary"  download style="text-decoration: none;"><ion-icon name="arrow-down-circle-outline" ></ion-icon></a>
          </div>
          <div class="card-footer text-muted">
           Hit me up !
          </div>
        </div>   

</template>

<script>
    export default {
        computed:{
            Education(){
                 return this.$store.state.Education
             }
         },
         mounted(){
             this.$store.dispatch('fetchEducation')
         }      
    }
    // VARIABLES
const elH = document.querySelectorAll(".timeline li > div");

// START
window.addEventListener("load", init);

function init() {
  setEqualHeights(elH);
}

// SET EQUAL HEIGHTS
function setEqualHeights(el) {
  let counter = 0;
  for (let i = 0; i < el.length; i++) {
    const singleHeight = el[i].offsetHeight;

    if (counter < singleHeight) {
      counter = singleHeight;
    }
  }

  for (let i = 0; i < el.length; i++) {
    el[i].style.height = `${counter}px`;
  }
}

</script>

<style scoped>
@import url("https://fonts.googleapis.com/css2?family=Inter:wght@400;700&display=swap");

* {
    box-sizing: border-box;
  }
  
  /* Set a background color */
  body {
    background-color: #474e5d;
    font-family: Helvetica, sans-serif;
  }
  
  
  .timeline::after {
    content: '';
    position: absolute;
    width: 6px;
    background-color: white;
    top: 0;
    bottom: 0;
    left: 50%;
    margin-left: -3px;
  }
  
  
  .container {
    padding: 10px 40px;
    position: relative;
    background-color: inherit;
    width: 50%;
  }
  
  
  .container::after {
    content: '';
    position: absolute;
    width: 25px;
    height: 25px;
    right: -17px;
    background-color: white;
    border: 4px solid #FF9F55;
    top: 15px;
    border-radius: 50%;
    z-index: 1;
  }
  
  .left {
    left: 0;
  }
  
  .right {
    left: 50%;
  }
  
  .left::before {
    content: " ";
    height: 0;
    position: absolute;
    top: 22px;
    width: 0;
    z-index: 1;
    right: 30px;
    border: medium solid white;
    border-width: 10px 0 10px 10px;
    border-color: transparent transparent transparent white;
  }
  
  .right::before {
    content: " ";
    height: 0;
    position: absolute;
    top: 22px;
    width: 0;
    z-index: 1;
    left: 30px;
    border: medium solid white;
    border-width: 10px 10px 10px 0;
    border-color: transparent white transparent transparent;
  }
  
  /* Fix the circle for containers on the right side */
  .right::after {
    left: -16px;
  }
  
  /* The actual content */
  .content {
    padding: 20px 30px;
    background-color: white;
    position: relative;
    border-radius: 6px;
  }
  
  /* Media queries - Responsive timeline on screens less than 600px wide */
  @media screen and (max-width: 600px) {
  /* Place the timelime to the left */
    .timeline::after {
      left: 31px;
    }
  
  /* Full-width containers */
    .container {
      width: 100%;
      padding-left: 70px;
      padding-right: 25px;
    }
  
  /* Make sure that all arrows are pointing leftwards */
    .container::before {
      left: 60px;
      border: medium solid white;
      border-width: 10px 10px 10px 0;
      border-color: transparent white transparent transparent;
    }
  
  /* Make sure all circles are at the same spot */
    .left::after, .right::after {
      left: 15px;
    }
  
  /* Make all right containers behave like the left ones */
    .right {
      left: 0%;
    }
  }
  
  



  
</style>