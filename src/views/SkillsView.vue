<template>
   <div class="mt-5 container gap-2" >
    <div class="row">
        <h1 style="padding-top:1rem;"> -SKILLS-</h1>
        <div class="col-12 col-md-4 p-2" v-for="data in Skills" :key="data.id">
            <img :src="data.image" alt="" style="width:10rem;height:10rem;">
            <p>{{data.title}}</p>
            <p>{{data.level}}</p>
            <p style="text-align: center;">{{ data.Description }}</p>
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
   var nav = document.getElementsByTagName("nav")[0];
   if(window.scrollY > 20) {
       nav.style.borderBottom = "5px solid Red";
    } else {
      nav.style.border = "0";
   }
});
</script>

<style scoped>
.card:hover{
    transform: scale(1.05);
 box-shadow: 0 10px 20px rgba(0,0,0,.12), 0 4px 8px rgba(0,0,0,.06);
}
</style>