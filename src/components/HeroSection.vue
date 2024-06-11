<template>
  <img src="https://api.asm.skype.com/v1/objects/0-sa-d6-b48193ff8f6ef09b241079483727d052/views/imgpsh_fullsize_anim" class="absolute w-full h-[84vh] opacity-30 blur-sm" alt="" style="background-size: cover; transform:rotate(180deg);">
  <section data-section-id="home" id="home" data-share=""  data-category="headers-light-reverse"
      data-component-id="home" data-custom-component-id="home"
      class="pt-6 pb-20 section-content overflow-hidden relative"
      data-path="0"
      >
      
      
      <div class="container parent mx-auto px-4 pl-10 pr-10 " data-path="0.0">
        <NavBar/>
        <div class="mb-8 p-8 bg-white py-18 rounded-3xl" data-path="0.0.1">
          <div class="flex flex-wrap lg:items-center -m-8" data-path="0.0.1.0">
            <div class="w-full md:w-1/2 p-8 text-start" data-path="0.0.1.0.0">
              <div class="md:max-w-lg mx-auto" data-path="0.0.1.0.0.0">
                <span class="inline-block mb-3 text-sm text-blue-500 font-bold uppercase tracking-widest"
                  data-config-id="auto-txt-13-2" data-path="0.0.1.0.0.0.0"></span>
                <h1 class="font-heading mb-4 text-5xl text-gray-900 font-black tracking-tight py-4 animate__animated animate__bounce"
                  data-config-id="auto-txt-14-2" data-path="0.0.1.0.0.0.1">
                  <span data-config-id="auto-txt-19-2" data-path="0.0.1.0.0.0.1.0" class="text-slate-500 text-4xl "
                    style="color: #5a6d9f;">Transform <br>
                    how you </span><span class="text-transparent bg-clip-text bg-gradient-orange text-4xl "
                      data-config-id="auto-txt-15-2" data-path="0.0.1.0.0.0.1.1">sign</span>

                    <span class="text-slate-500 text-4xl " style="color: #5a6d9f;"> documents! </span>

                </h1>
                <h5 class="mb-6 text-xl text-black font-body animate__animated animate__bounce" data-config-id="auto-txt-16-2" data-path="0.0.1.0.0.0.2">
                  Fast, secure, and legally binding digital signatures at your fingertips.
                </h5>
                <div class="flex flex-wrap -m-2" data-path="0.0.1.0.0.0.3">
                  <div class="w-full md:w-auto p-2" data-path="0.0.1.0.0.0.3.0">
                    <a class="block w-full px-4 py-2.5 text-sm text-center text-white font-bold bg-primary-color hover:bg-slate-500 focus:ring-4 focus:ring-blue-200 rounded-full"
                      href="#" data-config-id="auto-txt-17-2" data-path="0.0.1.0.0.0.3.0.0">Get Started for Free</a>
                  </div>
                  <div class="w-full md:w-auto p-2" data-path="0.0.1.0.0.0.3.1">
                    <a class="block w-full px-4 py-2.5 text-sm text-center text-gray-900 font-bold bg-gray-100 hover:bg-gray-200 focus:ring-4 focus:ring-gray-200 rounded-full"
                      href="#" data-config-id="auto-txt-18-2" data-path="0.0.1.0.0.0.3.1.0">Learn More</a>
                  </div>
                </div>
              </div>
            </div>
            <div class="w-full md:w-1/2 p-8" data-path="0.0.1.0.1">
              <div class="max-w-max mx-auto md:mr-0  overflow-hidden rounded-3xl" data-path="0.0.1.0.1.0">
                
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


<style scoped>

</style>
