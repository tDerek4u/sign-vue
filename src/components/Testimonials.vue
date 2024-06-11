<template>
       
    <section class="bg-gray-100" >
      <div class="w-full mx-auto max-w-xl flex flex-col justify-center py-24 relative p-8">
        <h1 class=" text-4xl flex justify-center w-full font-extrabold text-[#5A6D9F]"><span><i class="fa-solid fa-quote-left mr-2"></i></span>Testimonials <span><i class="fa-solid fa-quote-right ml-2"></i></span></h1>
        <div class="mt-6 border-t pt-12 max-w-xl mx-auto">
          <!-- Starts component -->
          <div class="flex flex-col w-full" x-data="{
               skip: 1,
               atBeginning: false,
               atEnd: false,
               next() {
                   this.to((current, offset) => current + (offset * this.skip))
               },
               prev() {
                   this.to((current, offset) => current - (offset * this.skip))
               },
               to(strategy) {
                   let slider = this.$refs.slider
                   let current = slider.scrollLeft
                   let offset = slider.firstElementChild.getBoundingClientRect().width
                   slider.scrollTo({ left: strategy(current, offset), behavior: 'smooth' })
               },
               focusableWhenVisible: {
                   'x-intersect:enter'() {
                       this.$el.removeAttribute('tabindex')
                   },
                   'x-intersect:leave'() {
                       this.$el.setAttribute('tabindex', '-1')
                   },
               },
               disableNextAndPreviousButtons: {
                   'x-intersect:enter.threshold.05'() {
                       let slideEls = this.$el.parentElement.children
                       // If this is the first slide.
                       if (slideEls[0] === this.$el) {
                           this.atBeginning = true
                       // If this is the last slide.
                       } else if (slideEls[slideEls.length-1] === this.$el) {
                           this.atEnd = true
                       }
                   },
                   'x-intersect:leave.threshold.05'() {
                       let slideEls = this.$el.parentElement.children
                       // If this is the first slide.
                       if (slideEls[0] === this.$el) {
                           this.atBeginning = false
                       // If this is the last slide.
                       } else if (slideEls[slideEls.length-1] === this.$el) {
                           this.atEnd = false
                       }
                   },
               },
           }">
            <div class="flex flex-col w-full" aria-labelledby="carousel-label" role="region" tabindex="0"
              x-on:keydown.left="prev" x-on:keydown.right="next">
              <h2 class="sr-only" hidden="" id="carousel-label">Carousel</h2>
              <span class="sr-only" hidden="" id="carousel-content-label">Carousel</span>
              <div class="items-center inline-flex lg:px-2 space-x-2">
                <button
                  class="bg-orange-500 hover:bg-orange-500 size-8 flex focus:bg-orange-500 rounded-full items-center text-white"
                  :class="{ 'opacity-50 ': atBeginning }" :aria-disabled="atBeginning" :tabindex="atEnd ? -1 : 0"
                  x-on:click="prev" tabindex="0" aria-disabled="true">
                  <span aria-hidden="true" class="mx-auto"> ← </span><span class="sr-only">Skip to previous slide
                    page</span>
                </button>
                <span class="bg-white rounded-full flex justify-center items-center font-bold w-12 h-8">{{ testimonials.length }}</span>
                <button
                  class="bg-orange-500 hover:bg-orange-500 size-8 flex focus:bg-orange-500 rounded-full items-center text-white"
                  :class="{ 'opacity-50 ': atEnd }" :aria-disabled="atEnd" :tabindex="atEnd ? -1 : 0" x-on:click="next"
                  tabindex="0">
                  <span aria-hidden="true" class="mx-auto"> → </span><span class="sr-only">Skip to next slide
                    page</span>
                </button>
              </div>
              <ul class="flex gap-3 overflow-hidden mt-4 scrollbar-hide snap-mandatory snap-x w-full rounded-2xl"
                role="listbox" aria-labelledby="carousel-content-label" tabindex="0" x-ref="slider">
                
                <li v-for="(testimonial, index) in testimonials" :key="index"
                  class="items-center justify-center w-full flex flex-col shrink-0 snap-start h-full p-8 rounded-2xl bg-white lg:p-10" 
                  role="option" x-bind="disableNextAndPreviousButtons">
                  <figure>
                    <div class="max-w-2xl">
                      <div class="flex flex-col text-start gap-12">
                        <p class="text-base text-gray-900 font-display text-balance">
                          {{ testimonial.text }}
                        </p>
                        <div class="block flex-shrink-0">
                          <div class="flex items-center">
                            
                            <div class="">
                              <p class="text-lg font-medium text-gray-700">
                                {{ testimonial.name }}
                              </p>
                              <p class="text-sm font-medium text-gray-500">
                                {{ testimonial.company }}
                              </p>
                            </div>
                          </div>
                        </div>
                      </div>
                    </div>
                  </figure>
                </li>
               
              </ul>
            </div>
          </div>
          <!-- Ends component -->
        </div>
      </div>
    </section>
    
    
</template>

<script>
export default {
    name: 'Testimonials',
    props: {
      msg: String
    },
    data() {
        return {
            testimonials : [
                {
                    name: 'Pepe Madrid',
                    company : 'CEO of Something INC',
                    text : `I've been using this services for years, and they
                          consistently exceed my expectations. The support
                          team is fantastic!`
                }
            ],
        }
    },
  }
</script>