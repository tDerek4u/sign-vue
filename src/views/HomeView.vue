<template>
  <div class="overflow-hidden wrapper" id="content">
    <HeroSection/>
    <Features/>
    <FAQ/>
    <Testimonials/>
    <Footer/>
  </div>
</template>

<script>
// @ is an alias to /src
import HeroSection from '@/components/HeroSection.vue'
import Features from '@/components/Features.vue'
import FAQ from '@/components/FAQ.vue'
import Testimonials from '@/components/Testimonials.vue'
import Footer from '@/components/Footer.vue'

export default {
  name: 'HomeView',
  components: {
    HeroSection,
    Features,
    FAQ,
    Testimonials,
    Footer
  }
}
</script>
