<template>
  <Navbar/>
  <div class="main">
    <img src="https://i.pinimg.com/564x/1a/4d/2d/1a4d2d4ba5ce714e800b23ba51fca297.jpg" id="homePIC">
    <h1>I'm Lithini Skhikhi <div class="roller">
      <span id="text">An<br/>
      Aspiring<br>
      Web Developer<br/></span>
      <br>
      <!-- <span id="spare-time">too much spare time?</span><br/> -->
      </div>
      </h1>
      <img src="https://i.pinimg.com/564x/f1/67/ad/f167add8e3fbef2fc46fb4b3d292376a.jpg" id="homePIC">
    </div>
    
</template>

<script>
// @ is an alias to /src
import HelloWorld from '@/components/HelloWorld.vue'

export default {
  name: 'HomeView',
  components: {
    HelloWorld
  }
}
</script>
<style src="../assets/css/styles.css">
body{
  background-color: black;
}
* {
  margin:0;
  padding:0;
  font-family: 'Arvo';
}



.main{
  height:100vh;
  width:100%;  
  display:flex;
  align-items:center;
  justify-content:center;
  text-align:center;
}
h1{
  text-align:center;
  text-transform: uppercase;
  color: #F1FAEE; 
  font-size: 4rem;
}

.roller{
  height: 4.125rem;
  line-height: 4rem;
  position: relative;
  overflow: hidden; 
  width: 100%;
  display: flex;
  justify-content: center;
  align-items: center;
  
  color: #1D3557;
}


#spare-time{
  font-size: 1rem;
  font-style: italic;
  letter-spacing: 1rem;
  margin-top: 0;
  color: #A8DADC;
  
}

.roller #text {
  position: absolute;
  top: 0;
  animation: slide 5s infinite;  
}

@keyframes slide {
  0%{
    top:0;
  }
  25%{
    top: -4rem;    
  }
  50%{
    top: -8rem;
  }
  72.5%{
    top: -12.25rem;
  }
}

@media screen and (max-width: 600px){
  h1{
  text-align:center;
  text-transform: uppercase;
  color: #F1FAEE; 
  font-size: 2.125rem;
}
  
  .roller{
  height: 2.6rem; 
  line-height: 2.125rem;  
  }
  
  #spare-time {
    font-size: 1rem;
    letter-spacing: 0.1rem;
  }
  
  .roller #text {  
  animation: slide-mob 5s infinite;  
}
  
  @keyframes slide-mob {
  0%{
    top:0;
  }
  25%{
    top: -2.125rem;    
  }
  50%{
    top: -4.25rem;
  }
  72.5%{
    top: -6.375rem;
  }
}
}
</style>