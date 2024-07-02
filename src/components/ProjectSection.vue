<template>
    <h1 class="headmain">Projects</h1>
        <div class="body" data-aos="flip-left"
     data-aos-easing="ease-out-cubic"
     data-aos-duration="2000" v-if="$store.state.projects.length > 0">
            <div class="row justify-content-center">
                <div class="card my-3" v-for="project in $store.state.projects" :key="project">
            <div class="poster">
                <img :src="project.image" alt="">
            </div>
            <div class="details">
                <h2>{{ project.name }}</h2>
                <div class="buttons">
                    <a :href="project.gitHub" target="_blank"><button class="mx-3 p-1">GitHub</button></a>
                    <a :href="project.vercel " target="_blank"><button class="mx-3 p-1 px-2">Live</button></a> 
                </div>
            </div>
        </div> 
            </div>
           
        </div>
    </template>

<style scoped>


.body{
    display: flex;
    justify-content: center;
    align-items: center;
    overflow-x: hidden;
}
.card{
    background-color: transparent;
    position: relative;
    max-width: 400px;
    height: 250px;
    overflow: hidden;
    border-radius: 10px;
    border: 0px;
}
.card .poster{
    position: relative;
    overflow: hidden;
}
.card .poster::before{
    content: '';
    position: absolute;
    bottom: -100px;
    width: 100%;
    height: 100%;
    background: linear-gradient(0deg,#0A1C3C 40%, transparent);
    transition: 0.5s;
    z-index: 1;
}
.card:hover .poster::before{
    bottom: 0px;
}
.card .poster img{
    width: 100%;
    height: 35vh;
    transition: 0.5s;
}
.card:hover .poster img{
    filter: blur(8px);
}
.card .details{
    position: absolute;
    width: 100%;
    left: 0;
    bottom: 0;
    z-index: 2;
    padding: 20px;
    transition: 0.5s;
}
.card .details .buttons{
    position: absolute;
    width: 100%;
    left: 0;
    bottom: -60px;
    z-index: 2;
    padding: 20px;
    transition: 0.5s;
    background: transparent;
    color: white;
}
.card:hover .details{
    bottom: 50px;
}
.card .details h2{
    color: rgb(255, 255, 255);
    font-size: 31px;
}
.card .details .buttons{
    margin-top: 15px;
}
.details .buttons a button{
    background: #0A1C3C;
    border: 2px solid rgb(255, 255, 255);
    color: rgb(255, 255, 255);
}
.details .buttons a button:hover{
    background: rgb(255, 255, 255);
    border: 2px solid rgb(255, 255, 255);
    color: #0A1C3C;
    transition: 0.3s;
}
@media screen and (width <600px){
    .proHead{
        margin-top: 20% !important;
    }
}
</style>