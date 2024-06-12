<template>
  <div class="overflow-hidden wrapper" id="content">
    <HeroSection/>
    <Features/>
    <Howitworks/>
    <FAQ/>
    <Testimonials/>
    <Footer/>
  </div>
</template>

<script>

import HeroSection from '@/components/HeroSection.vue'
import Features from '@/components/Features.vue'
import Howitworks from '@/components/Howitworks.vue' 
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
    Howitworks,
    Footer
  }
}
</script>
