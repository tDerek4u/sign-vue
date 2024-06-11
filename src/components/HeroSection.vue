<template>
  <section data-section-id="" id="home" data-share="" data-category="headers-light-reverse"
    data-component-id="26f94a33_02_awz" data-custom-component-id=""
    class="pt-6  pb-20 section-content overflow-hidden relative bg-gray-100" data-path="0">
    <div class="container parent mx-auto" data-path="0.0">
      <NavBar />      
      <div class="mb-8 p-8 bg-white rounded-3xl" data-path="0.0.1">
        <!-- Introduction Text Container -->
        <div class="flex flex-wrap p-12 gap-y-10 lg:items-center -m-8" data-path="0.0.1.0">
          <!-- Introduction Content -->
          <div class="w-full md:w-1/2 text-start" data-path="0.0.1.0.0">
            <div class="grid gap-5 md:max-w-lg mx-auto" data-path="0.0.1.0.0.0">
              <span data-config-id="auto-txt-19-2" data-path="0.0.1.0.0.0.1.0"
                class="primary-color font-extrabold text-4xl tracking-wide" style="color: #5a6d9f;">Transform <br>
                how you
                <span class="text-transparent bg-clip-text bg-gradient-orange" data-config-id="auto-txt-15-2"
                  data-path="0.0.1.0.0.0.1.1">sign</span>
                documents!
              </span>
              <p class="text-lg text-black tracking-tight" data-config-id="auto-txt-16-2" data-path="0.0.1.0.0.0.2">
                Fast, secure, and legally binding digital signatures at your fingertips.
              </p>
              <div class="flex flex-wrap -m-2" data-path="0.0.1.0.0.0.3">
                <div class="w-full md:w-auto p-2" data-path="0.0.1.0.0.0.3.0">
                  <a class="block w-full px-5 py-2.5 text-sm text-center text-white font-medium tracking-wide bg-primary-color hover:bg-slate-500 rounded-full"
                    href="#" data-config-id="auto-txt-17-2" data-path="0.0.1.0.0.0.3.0.0">Get Started for Free</a>
                </div>
                <div class="w-full md:w-auto p-2" data-path="0.0.1.0.0.0.3.1">
                  <a class="block w-full px-4 py-2.5 text-sm text-center text-black font-medium tracking-wide outline outline-2 outline-primary hover:bg-secondary-color hover:text-white rounded-full"
                    href="#" data-config-id="auto-txt-18-2" data-path="0.0.1.0.0.0.3.1.0">
                    Learn More
                  </a>
                </div>
              </div>
            </div>
          </div>
          <div class="flex w-full md:w-1/2 place-content-center" data-path="0.0.1.0.1">
            <div class="max-w-max mx-auto md:mr-0 bg-white overflow-hidden rounded-3xl" data-path="0.0.1.0.1.0">
              <img class="mx-auto" src="../assets/images/herosection_img.png" alt="" data-config-id="auto-img-3-2"
                data-path="0.0.1.0.1.0.0" />
            </div>
          </div>
        </div>
      </div>
      
    </div>
  </section>
</template>

<script>
import NavBar from './NavBar.vue';
export default {
  name: 'HeroSection',
  components: {
    NavBar
  },
  props: {
    msg: String
  }
}
</script>


<style scoped></style>
