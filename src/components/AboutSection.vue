<template>
   <div class="container">
     <div class="row justify-content-center mt-4">
         <h1 class="headmain">About</h1>
       <div v-if="about?.length">
         <p class="lead" v-for="(self, index) in about" :key="index">
           {{ self }}
         </p>
       </div>
       <Spinner v-else />
       <div class="row justify-content-center">
         <img
           src="https://kingbrink.github.io/all-images/images/photo.jpg"
           id="aboutimg"
           alt="profile"
           class="img-fluid shadow rounded-top"
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
 #aboutimg {
   width: 400px;
   height: 350px;
   margin-top: 15px;
   border-radius: 40px;
   display: inline-flex;
 }
 </style>
 