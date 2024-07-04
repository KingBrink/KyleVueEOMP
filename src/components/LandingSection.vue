<template>
    
   <div class="container-fluid home">
       <div class="img-box animate__animated animate__fadeInUp animate__slow" >
           <img src="https://kingbrink.github.io/all-images/images/kyle8.PNG" class="main-img" alt="" loading="lazy">
       </div>
       <div class="info animate__animated animate__fadeInDown animate__slow">
           <h1>I'm <span class="name">Kyle</span> Brink</h1>
           <p v-if="title">
               <span class="span"> {{ title }}</span>
           </p>
           <Spinner v-else/>
           <a class="button btn" href="#about">Learn More</a>

       <div class="footer-bar mx-4">
       <div class="btn-group">
           <a href="https://github.com/KingBrink" target="_blank" class="icons"><i class="bi bi-github"></i></a>
           <a href="https://www.linkedin.com/in/kyle-brink-3372232a0/" target="_blank" class="icons"><i class="bi bi-linkedin"></i></a>
       </div>
       </div>
       </div>
       
       </div>
 </template>
 <script setup>
 import Spinner from './Spinner.vue'
import { computed, onMounted, ref } from 'vue'
import { useStore } from 'vuex'
const store = useStore()
const jobTitle =
   computed(() => store.state.jobTitle)
const title = ref('a software developer')
const cnt = ref(-1)
function repeat() {
   try {
       if (cnt.value == jobTitle.value?.length) cnt.value = 0;
       title.value =
           jobTitle.value?.at(cnt.value)?.title;
       setTimeout(repeat, 2000)
       cnt.value++
   } catch (e) {
       //
   }
}
onMounted(() => {
   store.dispatch('fetchJobTitle')
   repeat()
})

 
 </script>
 <style scoped>
.button {
border: 1px solid black;
color: #fff;
text-shadow: 1px 1px black;
background-image: linear-gradient(30deg, #0400ff, #4ce3f7);
background-size: 100% auto;
font-family: inherit;
font-size: 17px;
padding: 0.6em 1.5em;
}

.button:hover {
background-position: right center;
background-size: 200% auto;
-webkit-animation: pulse 2s infinite;
animation: pulse512 1.5s infinite;
}

@keyframes pulse512 {
0% {
 box-shadow: 0 0 0 0 #05bada66;
}

70% {
 box-shadow: 0 0 0 10px rgb(218 103 68 / 0%);
}

100% {
 box-shadow: 0 0 0 0 rgb(218 103 68 / 0%);
}
}
.home{
   display: flex;
   justify-content: center;
   align-items:center ;
   gap: 250px;
 margin-top: 140px;

}

   .info h1{
       font-size: 70px;
       color: #212121; 
   }
   .info p {
       color: #606163;
       line-height: 22px;
       padding-top: 30px;
       font-size: 30px;
   }
   .info .button {
       display: inline-block;
        margin: 40px 0; 
       
   }
   
   .icons {
       font-size: 30px;
       color: #606163;
       margin-right: 15px;
       margin-left: 15px;
   }

   .icons:hover {
       color: blue;
   }


 
 .name{
     color: blue;
     }
     .img-box{
         background: url('https://kingbrink.github.io/all-images/images/wave8.png');
         background-size:cover;
         background-position: center;
         width: 500px;
         transition: bottom 1s, left 1s;
         }
         .main-img {
             width: 450px;
             
             }
           
   @media (min-width:300px) and (max-width:500px) {
       .home{
   display: flex;
   justify-content: center;
   align-items:center ;
   flex-direction: column;
   gap: 0px;
}   
.img-box{
         background: url('https://kingbrink.github.io/all-images/images/wave8.png');
         background-size:cover;
         background-position: center;
         width: 300px;
         transition: bottom 1s, left 1s;
         }
         .main-img {
             width: 250px;
             
             }
             .info h1{
       font-size: 40px;
       color: #212121; 
   }
   .info p {
       color: #606163;
       line-height: 25px;
       padding-top: 25px;
       font-size: 20px;
   }
   .info .button {
       display: inline-block;
        margin: 25px 0; 
       
   }
   
   .icons {
       font-size: 25px;
       color: #606163;
       margin-right: 15px;
       margin-left: 15px;
   }
}
@media (min-width:501px) and (max-width:699px) {
   .home{
       gap:80px;
   height: 50vh;
   }
   .img-box{
       background: url('https://kingbrink.github.io/all-images/images/wave8.png');
       background-size:cover;
       background-position: center;
       width: 500px;
   }
   .main-img {
       width: 250px;
      
   }
   .info h1{
       font-size: 40px;
       color: #212121;
   }
   .info p {
       color: #606163;
       line-height: 22px;
   }
   /* .info a {
       background: #212121;
       padding: 10px 18px;
       text-decoration: none;
       color: #fff;
       display: inline-block;
        margin: 30px 0; 
       border-radius: 5px;
   } */
   .icons{
       margin-left: 8%;
       margin-top: 100px;
   } 
   .icons {
       font-size: 30px;
       color: #606163;
       margin-right: 20px;
   }

}
@media (min-width:700px) and (max-width:900px){
    .home{
       gap:60px;
   height: 50vh;
   }
   .img-box{
       background: url('https://kingbrink.github.io/all-images/images/wave8.png');
       background-size:cover;
       background-position: center;
       width: 500px;
   }
   .main-img {
       width: 250px;
      
   }
   .info{
    height: 300px;
   }
   .info h1{
       font-size: 40px;
       color: #212121;
   }
   .info p {
       color: #606163;
       line-height: 22px;
   }
   /* .info a {
       background: #212121;
       padding: 10px 18px;
       text-decoration: none;
       color: #fff;
       display: inline-block;
        margin: 30px 0; 
       border-radius: 5px;
   } */
   .icons{
       margin-left: 8%;
       margin-top: 0px;
   } 
   .icons {
       font-size: 30px;
       color: #606163;
       margin-right: 20px;
   }
   /* button {
 margin: 0px 0px;
 padding: 0px 0px;
 background-size: 70%;
} */
.span{
    font-size: 20px;
}

} 
/* 
button {
 display: flex;
 align-items: center;
 justify-content: center;
 gap: 10px;
 padding: 0 10px;
 color: white;
 text-shadow: 2px 2px rgb(116, 116, 116);
 text-transform: uppercase;
 cursor: pointer;
 border: solid 2px black;
 letter-spacing: 1px;
 font-weight: 600;
 font-size: 17px;
 background-color: hsl(49deg 98% 60%);
 border-radius: 50px;
 position: relative;
 overflow: hidden;
 transition: all 0.5s ease;
} */

button:active {
 transform: scale(0.9);
 transition: all 100ms ease;
}

button svg {
 transition: all 0.5s ease;
 z-index: 2;
}

.play {
 transition: all 0.5s ease;
 transition-delay: 300ms;
}

button:hover svg {
 transform: scale(3) translate(50%);
}

.now {
 position: absolute;
 left: 0;
 transform: translateX(-100%);
 transition: all 0.5s ease;
 z-index: 2;
}

button:hover .now {
 transform: translateX(10px);
 transition-delay: 300ms;
}

button:hover .play {
 transform: translateX(200%);
 transition-delay: 300ms;
}

 </style>
