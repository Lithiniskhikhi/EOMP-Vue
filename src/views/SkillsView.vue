<template>
   <div class="mt-5 container gap-2" >
    <div class="row">
        <h1 style="padding-top:3rem;">MY SKILLS</h1>
        <div class="col-12 col-md-6" v-for="data in Skills" :key="data.id">
            <img :src="data.image" alt="" style="width:10rem;height:10rem;">
            <p>{{data.title}}</p>
            <p>{{data.level}}</p>
            <p>{{ data.Description }}</p>
         </div>
    </div>
</div>
</template>

<script>
    export default {
        computed:{
            Skills(){
                return this.$store.state.Skills
            }
        },
        mounted(){
            this.$store.dispatch('fetchSkills')
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