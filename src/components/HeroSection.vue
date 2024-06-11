<template>
  <section data-section-id="" id="home" data-share="" data-category="headers-light-reverse"
      data-component-id="26f94a33_02_awz" data-custom-component-id=""
      class="pt-6  pb-20 section-content overflow-hidden relative bg-gray-100"
      data-path="0"
      >
      <div class="container parent mx-auto px-4 pl-10 pr-10" data-path="0.0">
        <NavBar/>
        <div class="mb-8 p-8 bg-white rounded-3xl" data-path="0.0.1">
          <div class="flex flex-wrap lg:items-center -m-8" data-path="0.0.1.0">
            <div class="w-full md:w-1/2 p-8 text-start" data-path="0.0.1.0.0">
              <div class="md:max-w-lg mx-auto" data-path="0.0.1.0.0.0">
                <span class="inline-block mb-3 text-sm text-blue-500 font-bold uppercase tracking-widest"
                  data-config-id="auto-txt-13-2" data-path="0.0.1.0.0.0.0"></span>
                <h1 class="font-heading mb-4 text-5xl text-gray-900 font-black tracking-tight"
                  data-config-id="auto-txt-14-2" data-path="0.0.1.0.0.0.1">
                  <span data-config-id="auto-txt-19-2" data-path="0.0.1.0.0.0.1.0" class="text-slate-500 text-4xl "
                    style="color: #5a6d9f;">Transform <br>
                    how you </span><span class="text-transparent bg-clip-text bg-gradient-orange text-4xl "
                      data-config-id="auto-txt-15-2" data-path="0.0.1.0.0.0.1.1">sign</span>

                    <span class="text-slate-500 text-4xl " style="color: #5a6d9f;"> documents! </span>

                </h1>
                <p class="mb-6 text-xl text-black" data-config-id="auto-txt-16-2" data-path="0.0.1.0.0.0.2">
                  Fast, secure, and legally binding digital signatures at your fingertips.
                </p>
                <div class="flex flex-wrap -m-2" data-path="0.0.1.0.0.0.3">
                  <div class="w-full md:w-auto p-2" data-path="0.0.1.0.0.0.3.0">
                    <a class="block w-full px-4 py-2.5 text-sm text-center text-white font-bold bg-orange-400 hover:bg-orange-500 focus:ring-4 focus:ring-blue-200 rounded-full"
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
              <div class="max-w-max mx-auto md:mr-0 bg-white overflow-hidden rounded-3xl" data-path="0.0.1.0.1.0">
                <img class="mx-auto" src="../assets/images/herosection_img.png" alt="" data-config-id="auto-img-3-2"
                  data-path="0.0.1.0.1.0.0" />
              </div>
            </div>
          </div>
        </div>
        <div class="px-2 py-6 bg-white rounded-3xl" data-path="0.0.2">
          <h1 class="flex justify-center mb-2 text-2xl">Why Choose Us!</h1>
          
          <div class="xl:flex lg:flex md:grid md:grid-cols-2 md:gap-3 col  p-4 justify-center " data-path="0.0.2.0">
            <div class="bg-zinc-100 rounded-2xl text-start mt-2 p-4 h-auto xl:w-1/4 lg:w-1/4 w-auto mb-2 sm:mb-0 sm:mr-2">
              <div class="flex">
                <img src="../assets/images/lock.png" alt=""/>
                <span class="mt-2 ms-3">Unmatched Security</span>
              </div> <br>
              <p>Your documents are encrypted and stored securely.</p>
            </div>
            <div class="bg-zinc-100 rounded-2xl text-start mt-2 p-4  h-auto xl:w-1/4 lg:w-1/4 w-auto mb-2 sm:mb-0 sm:mr-2">
              <div class="flex">
                <img src="../assets/images/lock_2.png" alt=""/>
                <span class="mt-2 ms-3">Time-Saving</span>
              </div><br>
              <p>Sign documents instantly from anywhere.</p>
            </div>
            <div class="bg-zinc-100 rounded-2xl text-start mt-2 p-4  h-auto xl:w-1/4 lg:w-1/4 w-auto mb-2 sm:mb-0 sm:mr-2">
              <div class="flex">
                <img src="../assets/images/lock.png" alt=""/>
                <span class="mt-2 ms-3">Legally Binding</span>
              </div><br>
              <p>Complies with e-signature laws worldwide.</p>
            </div>
            <div class="bg-zinc-100 rounded-2xl text-start mt-2 p-4  h-auto xl:w-1/4 lg:w-1/4 w-auto mb-2 sm:mb-0 sm:mr-2">
              <div class="flex">
                <img src="../assets/images/user_frendly.png" alt=""/>
                <span class="mt-2 ms-3">User-Friendly</span>
              </div><br>
              <p>Intuitive interface designed for ease of use.</p>
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
