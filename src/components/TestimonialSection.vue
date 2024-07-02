<template>
  <h1 class="headmain">Testimonials</h1>
  <div class="container  ">
    <div class="row" v-if="$store.state.testimonials.length > 0">
      <div class="peeps col-md-4 my-3" v-for="testimonial in $store.state.testimonials"
      :key="testimonial">
      <div
        class="person"
       
      >
        <div class="lines"></div>
        <div class="cardImage">
          <img :src="testimonial.profile" />
        </div>
        <div class="content">
          <div class="details mx-2">
            <h2>{{ testimonial.name }} {{ testimonial.surname }}</h2>
            <h6 class=" role">{{ testimonial.role }}</h6>
            <div class="speech">{{ testimonial.quotes }}</div>
          </div>
        </div>
      </div>
    </div>
    </div>
  </div>
</template>
<style scoped>
.tests {
  text-align: left;
  mix-blend-mode: difference;
  font-size: clamp(2.8rem, 5vw, 6.5rem);
}
.row {
  justify-content: center;
}
.prac {
  background: red;
  height: 100px;
  width: 100px;
}
.peeps {
  /* justify-content: center !important; */
  text-align: left;
  width: 400px;
}
.container {
  overflow-x: hidden;
}
.person {
  margin-top: 20%;
  position: relative;
  min-width: 300px;
  height: 520px;
  background: black;
  color: orangered;
  /* transition: 0.5s; */
}
.person .lines {
  position: absolute;
  inset: 0;
  background: black;
  overflow: hidden;

}
.person .lines::before {
  content: "";
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  width: 700px;
  height: 200px;
  background: linear-gradient(
    transparent,
    rgb(255, 0, 0),
    rgb(255, 0, 0),
    transparent
  );
  animation: animate 8s linear infinite;
}
@keyframes animate {
  0% {
    transform: translate(-50%, -50%) rotate(0deg);
  }
  100% {
    transform: translate(-50%, -50%) rotate(360deg);
  }
}
.person .lines::after {
  content: "";
  position: absolute;
  inset: 0px;
  background: #0F4C75;
  border: 4px solid black;
}
.person .cardImage {
  position: absolute;
  top: -50px;
  left: 50%;
  transform: translateX(-50%);
  width: 250px;
  height: 250px;
  transition: 0.5s;
  z-index: 10;
  overflow: hidden;
}

.person .cardImage::after {
  content: "";
  position: absolute;
  inset: 0px;
  background: rgb(0, 0, 0);
}
.person .cardImage img {
  position: absolute;
  top: 5px;
  left: 5px;
  z-index: 1;
  width: calc(96.5%);
  height: calc(96.5%);
}
.person .content {
  padding: 10px;
  position: absolute;
  width: 100%;
  height: 100%;
  display: flex;
  justify-content: center;
  align-items: center;
  overflow: hidden;
  gap: 30px;
}
.person .content h2 {
  font-weight: 600;
  margin-top: 175px;
  color: #F2FBD5;
}
.card .content .details {
  padding: 3%;
  /* font-size: 1.25em; */
}

.role {
  font-weight: 500;
  color: #42CFC7;
}
.speech {
  font-weight: 500;
  margin-top: 3%;
  color: #F2FBD5;
}
@media screen and (width <= 770px) {
  .peeps {
    justify-content: center !important;
  }
}

@media screen and (width <= 375px) {
  .peeps {
    min-width: 300px;
    margin-right: 15px;
  }
}
</style>
