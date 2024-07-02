<template>
  <div class="wrapper">
    <NavBar />
    <main class="container-fluid">
      <router-view />
    </main>
    <Footer />
  </div>
</template>
<script>
import NavBar from '@/components/NavBar.vue'
import Footer from '@/components/Footer.vue'
export default {
  components: {
    NavBar,
    Footer,
  },
  computed:{
    getHome(){
      return this.$store.dispatch("getHome")
    },
    getAbout(){
      return this.$store.dispatch("getAbout")
    },
    getResume(){
      return this.$store.dispatch("getResume")
    },
    getSkills(){
      return this.$store.dispatch("getSkills")
    },
    getProjects(){
      return this.$store.dispatch("getProjects")
    },
    getTestimonials(){
      return this.$store.dispatch("getTestimonials")
    },
    getContact(){
      return this.$store.dispatch("getContact")
    }
  },
mounted(){
  this.getHome
  this.getAbout
  this.getResume
  this.getSkills
  this.getProjects
  this.getTestimonials
  this.getContact
},
} 


</script>

<style src="@/assets/css/style.css">

</style>
