<template>
    <div>
     <h1>-Education- </h1> 
    </div>
<br>
        <div class="container left" v-for="data in Education" :key="data.id" style="width:25rem;">
          <div class="content">
            <h2>2017</h2>
            <img :src="data.image" alt="" >
                    <p style="color:black">{{data.title}}</p>
                    <p style="color:black">{{data.Timeline}}</p>
                    <p style="color:black">{{ data.Description }}</p>
          </div>
        </div>
        
      
<h2>Download my cv</h2>
<br>
<button style="border-radius: 30%;width:5rem"><ion-icon name="arrow-down-circle-outline" style="height:3rem"></ion-icon></button>
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
  
  /* The actual timeline (the vertical ruler) */
 
  /* The actual timeline (the vertical ruler) */
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
  
  /* Container around content */
  .container {
    padding: 10px 40px;
    position: relative;
    background-color: inherit;
    width: 50%;
  }
  
  /* The circles on the timeline */
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
  
  /* Place the container to the left */
  .left {
    left: 0;
  }
  
  /* Place the container to the right */
  .right {
    left: 50%;
  }
  
  /* Add arrows to the left container (pointing right) */
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
  
  /* Add arrows to the right container (pointing left) */
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