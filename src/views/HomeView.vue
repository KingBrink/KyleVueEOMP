<template>
  <div class=" body container">
    <section class="row" id="landing">
      <LandingSection />
    </section>
    <section class="row" id="about">
      <AboutSection />
    </section>
    <section class="row">
      <ResumeSection/>

    </section>
    <section class="row" id="testimonials">
      <TestimonialSection/>
      

    </section>
    <section class="row" id="projects">
      <ProjectSection/>

    </section>
    <section class="row" id="reachMe">
      <ContactSection/>

    </section>
  </div>
</template>

<script>
import LandingSection from '@/components/LandingSection.vue'
import AboutSection from '@/components/AboutSection.vue'
import ResumeSection from '@/components/ResumeSection.vue'
import TestimonialSection from '@/components/TestimonialSection.vue'
import ProjectSection from '@/components/ProjectSection.vue'
import ContactSection from '@/components/ContactSection.vue'
export default {
  name: 'HomeView',
  components: {
    LandingSection,
    AboutSection,
    ResumeSection,
    TestimonialSection,
    ProjectSection,
    ContactSection
  }
}
</script>

