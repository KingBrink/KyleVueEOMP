<template>
  <section class="mt-5">
    <h1 class="headmain" id="resume">Resume</h1>
    <div class="resCont" style="display:inline-block;">
        <div class="justify-content-center mx-2">
        <div class="row my-5 resRow"  v-for="resum in $store.state.resume" :key="resum">
          <div class="col-md-6 my-5" data-aos="fade-up" data-aos-duration="1200" style="text-align: left;">
                    <h6 class="my-4 text-primary" style=" margin-bottom: 20px;">📅  {{ resum.year }}</h6>
              <a class="personLink"><h2>{{ resum.place }}</h2></a>
              <div class="desc">{{ resum.description}}</div>
            </div>
            <div class="col-md-6 imgCol my-5">
              <img :src="resum.logo" alt="">
            </div>
    </div>
    <a href="https://drive.google.com/file/d/1HyCDXu4-tDWUk5YZif4hL1hUqTS9q7EB/view?usp=sharing" target="_blank"><button class="btn">
DOWNLOAD CV
</button></a>


    </div>
    </div>
    <div class="skilldiv" data-aos="zoom-in">
      <h1 class="headmain">Skills</h1>
    <div class="container-lg mt-4" style="display:inline-block;">
        <div class="row justify-content-center mx-2">
        <div class="col-md-2 mx-2 my-2 skillsCol"   v-for="skill in $store.state.skills" :key="skill">
                  <img :src="skill.skill" alt="">
    </div>
    </div>
    </div>
    </div>
  </section>
</template>




<style scoped>


.skilldiv{
margin-top: 25px;
}
.btn {
font-size: 1.2rem;
padding: 1rem 2.5rem;
border: none;
outline: none;
border-radius: 0.4rem;
cursor: pointer;
text-transform: uppercase;
background-color: rgb(14, 14, 26);
color: rgb(234, 234, 234);
font-weight: 700;
transition: 0.6s;
box-shadow: 0px 0px 60px #1f4c65;

}

.btn:active {
scale: 0.92;
}

.btn:hover {
background: rgb(2,29,78);
background: linear-gradient(270deg, rgba(2, 29, 78, 0.681) 0%, rgba(31, 215, 232, 0.873) 60%);
color: rgb(4, 4, 38);
}

.resCont{
width: 100%;
}


.skillsH1{
text-align: left;
mix-blend-mode: difference;
font-size: clamp(3.4rem, 5vw, 6.5rem);
}

.resRow{
color: rgb(18, 64, 231);
/* mix-blend-mode: difference; */
justify-content: center !important;
align-items: center !important;
}

.resRow img{
max-width: 150px;
}
.desc{
/* mix-blend-mode: difference; */
margin-top: 4%;
color: black;
}

.skillsCol{
  height: 20vh;
  /* mix-blend-mode: luminosity; */
}
.skillsCol img{
  margin-top: 5%;
  max-width: 100%;
  max-height: 80%;
}
/* .skillsCol:hover{
mix-blend-mode: unset;
} */

.personLink{
text-decoration: none;
color: blue;
}

.personLink h2:hover{
color: rgb(0, 76, 255);
transition: 0.5s;
}

@media screen and (width < 1000px) {

.introH1{
  font-size: 3rem !important;
}

.meImg{
  max-height: 615px;
}
}

@media screen and (width < 768px) {
.ImgCol{
  display: none;
}

.introH1{
  margin-top: 30vh;
font-size: clamp(3.4rem, 5vw, 5rem);
}
.skillsCol img{
  margin-top: 2% !important;
}
}
@media screen and (width < 425px) {
.skillsCol img{
  margin-top: 5% !important;
}
}
</style>