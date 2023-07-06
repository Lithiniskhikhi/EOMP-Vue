<template>
    <div>
        <div class="layout">

            <div class="card card1">
                <div class="blog-img">
                  <h2 class="card-heading">SkinC</h2>
                  <div class="content">
                  <pre class="pre">This was a collaborative project with Rabia Haucha it we used Javascript and stored objects in a local storage</pre>
        
                </div>
              </div>
              <a href="#blog1" class="darksoul-a"><button class="button" type="button"><div style="display: flex; color:black"><p style="color:black;">Visit Github! <b></b></p></div></button></a>
              <a href="#blog1" class="darksoul-a"><button class="button" type="button"><div style="display: flex; color:black"><p style="color:black;">Visit Netlify! <b></b></p></div></button></a>
              <a href="#blog1" class="darksoul-a"><button class="button" type="button"><div style="display: flex; color:black"><p style="color:black;">Visit Visit Firebase! <b></b></p></div></button></a>
        
            </div>
        
            <div class="card card2">
              <div class="blog-img">
                <h2 class="card-heading">Calculator</h2>
                <div class="content">
                <pre class="pre">This calculator was built using Javascript and Html it is fully functional
        
                </pre> 
              </div>
              </div>
              <a href="#blog1" class="darksoul-a"><button class="button" type="button"><div style="display: flex; color:black"><p style="color:black;">Visit Github! <b></b></p></div></button></a>
              <a href="#blog1" class="darksoul-a"><button class="button" type="button"><div style="display: flex; color:black"><p style="color:black;">Visit Netlify! <b></b></p></div></button></a>
              <a href="#blog1" class="darksoul-a"><button class="button" type="button"><div style="display: flex; color:black"><p style="color:black;">Visit Visit Firebase! <b> </b></p></div></button></a>
            
            </div>
        
            <div class="card card3">
              <div class="blog-img">
                <h2 class="card-heading">E-commerce</h2>
                <div class="content">
                <pre class="pre">E-commerce project was built using mainly javascript its objects<br> are stored in a json server</pre>
                </div>
              </div>
              <a href="" class="darksoul-a"><button class="button" type="button"><div style="display: flex; color:black"><p style="color:black;">Visit Github! <b></b></p></div></button></a>
              <a href="" class="darksoul-a"><button class="button" type="button"><div style="display: flex; color:black"><p style="color:black;">Visit Netlify! <b></b></p></div></button></a>
              <a href="" class="darksoul-a"><button class="button" type="button"><div style="display: flex; color:black"><p style="color:black;">Visit Visit Firebase! <b></b></p></div></button></a>
            
            </div>
        
            <div class="card card4">
              <div class="blog-img">
                <h2 class="card-heading">BMI calculator</h2>
                <div class="content">
                  <pre class="pre">this can calculate a persons BMI <br> and</pre>
                </div>
              </div>
              <a href="" class="darksoul-a"><button class="button" type="button"><div style="display: flex; color:black"><p style="color:black;">Visit Github! <b></b></p></div></button></a>
              <a href="" class="darksoul-a"><button class="button" type="button"><div style="display: flex; color:black"><p style="color:black;">Visit Netlify! <b></b></p></div></button></a>
              <a href="" class="darksoul-a"><button class="button" type="button"><div style="display: flex; color:black"><p style="color:black;">Visit Visit Firebase! <b></b></p></div></button></a>
            
            </div>
          
            
            <div class="card card5">  
              <div class="blog-img">
                
                <h2 class="card-heading">Projects</h2>
                <div class="content">
                  <pre class="pre">Quantum computing is a place 
        of pc technological know-how that makes 
        use of the ideas of quantum theory...
        <b class="bold">Read the blog to know more about<br />Calculator</b> </pre>
        
                </div>
               
                
              </div>
              <a href="" class="darksoul-a"><button class="button" type="button"><div style="display: flex; color:black"><p style="color:black;">Visit Github! <b></b></p></div></button></a>
              <a href="" class="darksoul-a"><button class="button" type="button"><div style="display: flex; color:black"><p style="color:black;">Visit Netlify! <b></b></p></div></button></a>
              <a href="" class="darksoul-a"><button class="button" type="button"><div style="display: flex; color:black"><p style="color:black;">Visit Visit Firebase! <b></b></p></div></button></a>
        
            </div>
        <br>
          
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
@import url('https://fonts.googleapis.com/css2?family=Josefin+Sans&family=Luckiest+Guy&display=swap');
 body
 {
   height: 100vh;
   width: 100%;
 }
 .layout{
        position: relative;
        margin-top: 15%;
        margin-left: 25%;
         
       }
       .layout:hover .card{
         
         filter: blur(3px);
       }
       .layout .card:hover{
         filter: blur(0px);
         opacity: 1;
         
       }

       .scroll {
        max-height: 100px;
        overflow-y: auto;
    }
    
       .card {
         box-shadow: 0.5px 1px 8px 0 rgba(0,0,0,0.2);
           transition: 0.3s;
           width: 300px;
           height: 450px;
           border-radius: 5px;
           margin: 25px;
           font-family: 'Josefin Sans', sans-serif;
           font-size: large;
           display: flex;
           flex-direction: column;
           position: absolute;
         
       }
         .card1 {
           transform: rotate(-20deg);
           background-color: white;
           margin-left: -2px;
           top: 20px;
           
 
        }
         .card1:hover {
           box-shadow: 1px 2px 16px 0 rgba(0,0,0,0.2);
           transform: translateY(-200px);
        
           z-index: 100;
         }
 
         .card2 {
           z-index: 5;
           margin-left: 100px;
           transform: rotate(-10deg);
           top: 10px;
           background-color: white;
           
        }
         .card2:hover {
           box-shadow: 1px 2px 16px 0 rgba(0,0,0,0.2);
           transform: translateY(-200px);
           z-index: 100;
         }
 
         .card3 {
           z-index: 10;
           margin-left: 200px;
           transform: rotate(-3deg);
           top: 0px;
           background-color: white;
        }
         .card3:hover {
           box-shadow: 1px 2px 16px 0 rgba(0,0,0,0.2);
           transform: translateY(-200px);
           z-index: 100;
         }
 
         .card4 {
           z-index: 20;
           margin-left: 300px;
           transform: rotate(10deg);
           background-color: white;
           top: 20px;
        }
         .card4:hover {
           box-shadow: 1px 2px 16px 0 rgba(0,0,0,0.2);
           transform: translateY(-200px);
           z-index: 100;
         }
           .card5 {
           /* box-shadow: 0.5px 1px 8px 0 rgba(0,0,0,0.2);
           transition: 0.3s;
           width: 300px;
           height: 450px;
           border-radius: 5px;
           margin: 25px;
           font-family: 'Josefin Sans', sans-serif;
           font-size: large;
           display: flex;
           flex-direction: column;
           position: absolute; */
           z-index: 30;
           margin-bottom: 0px;
           margin-left: 400px;
           transform: rotate(20deg);
           background-color: white;
           top: 50px;
        }
         .card5:hover {
           box-shadow: 1px 2px 16px 0 rgba(0,0,0,0.2);
           transform: translateY(-200px);
           z-index: 100;
         }
         .blog-img{
             height: 250px;
            display: flex;
             background: rgb(255,255,255);
 background: linear-gradient(7deg, rgba(255,255,255,1) 12%, rgba(231,224,255,1) 12%, rgba(244,227,253,1) 46%, rgba(255,222,255,1) 69%, rgba(255,226,250,1) 83%, rgba(255,225,245,1) 93%, rgba(255,210,240,1) 100%);
 
             
         }
         .card-heading
       {
     color: rgb(108, 60, 139);
         transform: rotate(270deg);
         width: fit-content;
         height: fit-content;
         margin-top: 30%;
         margin-left: -9%;
         margin-right: 100%;
 font-family: 'Luckiest Guy', cursive;
       }
       .content
 {
     display: none;
     
 }
 .card1:hover .content
 {
   display: flex;
   margin-top: 30%;
         margin-left: -9%;
         margin-right: 50%;
 }
 .card2:hover .content
 {
   display: flex;
   margin-top: 30%;
         margin-left: -9%;
         margin-right: 50%;
 }
 .card3:hover .content
 {
   display: flex;
   margin-top: 30%;
         margin-left: -9%;
         margin-right: 50%;
 }
 .card4:hover .content
 {
   display: flex;
   margin-top: 30%;
         margin-left: -9%;
         margin-right: 50%;
 }
 .card5:hover .content
 {
   display: flex;
   margin-top: 30%;
         margin-left: -9%;
         margin-right: 50%;
 }
        
  pre
  {
   margin-left: -10%;
   font-family: 'Josefin Sans', sans-serif;
   font-size: large;
   color: rgb(108, 60, 139);
  }
  
  .button
  {
   display: none;
   margin: auto;
   height: fit-content;
   width: fit-content;
   border-radius: 5px;
   background: none;
   font-size: 16px;
   cursor: pointer;
   border: none;
   color: rgb(108, 60, 139);
   font-family: 'Josefin Sans', sans-serif;
   font-size: large;
   
  }
  .arrow
  {
   display: none;
   margin: auto;
   height: fit-content;
   width: 30px;
  }
  .button:hover
  {
   box-shadow: none;
 background: none;
 transform: scale(1.05);
  }
  .button:hover .arrow {
 
   color: rgb(108, 60, 139);
  display: block;
  }
 
  .card1:hover .button
 {
   display: flex;
  
 }
 .card2:hover .button
 {
   display: flex;
 
 }
 .card3:hover .button
 {
   display: flex;
  
 }
 .card4:hover .button
 {
   display: flex;
 
 }
 .card5:hover .button
 {
   display: flex;
  
 }
 
 .darksoul-a
         {
           color: rgb(108, 60, 139);
           text-decoration: none; 
           margin: auto;
           
         }
         .bold
         {
           color: rgb(108, 60, 139);
         }
 
</style>