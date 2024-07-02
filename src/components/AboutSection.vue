<template>
  <div class="about-space"></div>
   <div class="container" data-aos="fade-down-right">
     <div class="row justify-content-center mt-4">
         <h1 class="headmain">About</h1>
       <div v-if="about?.length">
         <p class="lead" v-for="(self, index) in about" :key="index">
           {{ self }}
         </p>
       </div>
       <Spinner v-else />
       <div class="row justify-content-center text-center">
         <img
           src="https://kingbrink.github.io/all-images/images/photo.jpg"
           id="aboutimg"
           alt="profile"
           class="img-fluid"
           loading="lazy"
         />
       </div>
     </div>
   </div>
 </template>
 
 <script setup>
 import Spinner from "./Spinner.vue";
 import { computed, onMounted } from "vue";
 import { useStore } from "vuex";
 const store = useStore();
 const about = computed(() => store.state.about);
 
 onMounted(() => {
   store.dispatch("fetchAbout");
 });
 </script>
 
 <style scoped>
 .about-space{
  padding: 50px;
 }
 #aboutimg {
   width: 400px;
   height: 500px;
   margin-top: 15px;
   border-radius:100%;
   display: inline-flex;
 }

 @media (min-width:300px) and (max-width:500px){
  #aboutimg {
   width: 200px;
   height: 200px;
   margin-top: 15px;
   border-radius:100%;
   display: inline-flex;
 }
 .lead{
  font-size:18px;
 }
 }


 </style>
 