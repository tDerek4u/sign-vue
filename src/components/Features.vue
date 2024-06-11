<template>
  <!-- Features -->
  <section class=" overflow-hidden bg-gray-100 rounded-tl-3xl rounded-br-3xl " id="features">
    <div class="pb-14 container mx-auto">
      <div class="px-10 py-6 bg-white rounded-3xl" data-path="0.0.2">
        <h1 class="flex justify-center my-4 text-3xl font-extrabold primary-color">
          <i class="fa-solid fa-house"></i>Why Choose Us!
        </h1>
        <div class="xl:flex lg:flex md:grid md:grid-cols-2 md:gap-3 col justify-center " data-path="0.0.2.0">
          <div class="bg-zinc-100 rounded-2xl text-start mt-2 p-4 h-auto xl:w-1/4 lg:w-1/4 w-auto mb-2 sm:mb-0 sm:mr-2">
            <div class="flex">
              <i class="fa-user"></i>
              <span class="mt-2 ms-3">Unmatched Security</span>
            </div> <br>
            <p>Your documents are encrypted and stored securely.</p>
          </div>
          <div
            class="bg-zinc-100 rounded-2xl text-start mt-2 p-4  h-auto xl:w-1/4 lg:w-1/4 w-auto mb-2 sm:mb-0 sm:mr-2">
            <div class="flex">
              <img src="../assets/images/lock_2.png" alt="" />
              <span class="mt-2 ms-3">Time-Saving</span>
            </div><br>
            <p>Sign documents instantly from anywhere.</p>
          </div>
          <div
            class="bg-zinc-100 rounded-2xl text-start mt-2 p-4  h-auto xl:w-1/4 lg:w-1/4 w-auto mb-2 sm:mb-0 sm:mr-2">
            <div class="flex">
              <img src="../assets/images/lock.png" alt="" />
              <span class="mt-2 ms-3">Legally Binding</span>
            </div><br>
            <p>Complies with e-signature laws worldwide.</p>
          </div>
          <div
            class="bg-zinc-100 rounded-2xl text-start mt-2 p-4  h-auto xl:w-1/4 lg:w-1/4 w-auto mb-2 sm:mb-0 sm:mr-2">
            <div class="flex">
              <img src="../assets/images/user_frendly.png" alt="" />
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
export default {
  name: 'Features',
  props: {
    msg: String
  }
}
</script>

<style scoped></style>