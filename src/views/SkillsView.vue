<template>
   <div class="mt-5 container">
    <div class="row">
        <h1 style="padding-top:3rem;">MY SKILLS</h1>
        <div class="col-12 col-md-6" v-for="data in Skills" :key="data.id">
            <img :src="data.image" alt="" style="width:6rem;height:6rem;">
            <p>{{data.title}}</p>
            <p>{{ data.description }}</p>
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
</script>

<style scoped>

</style>