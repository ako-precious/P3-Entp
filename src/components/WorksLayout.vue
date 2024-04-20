<template>
  <section class="z-20 relative workssection py-12 min-h-screen bg-orange overflow-hidden" id="works" :style="{ transform: `translateY(${translateX}px)` }">
    <div class="container m-auto bg-transparent flex flex-col ">
      <div class="w-full relative">
        <div class="flex m-auto">
          <h1
            :style="{ transform: `translateX(${translateX}px)` }"
            role="heading"
            class="sticky float-right worksheader whitespace-nowrap w-full leading-10 pb-4 lg:text-6xl md:text-5xl text-white text-3xl font-bold capitalize transition-all"
          >
            <span>
             Who we are</span
            >
          </h1>
        </div>
      </div>
    </div>
    <!-- <WorksPhone /> -->
    <div class="container  relative flex flex-col justify-center items-center m-auto">
        <div v-motion-slide-visible-left :delay="300" class="flex flex-col lg:flex-row items-center pt-12 lg:gap-6">
      
        <h1
          data-jarallax-element="0 -200"
          class="hover-3 leading-10 text-left mb-6 md:text-2xl lg:w-1/2 text-white text-2xl font-bold capitalize transition-all delay-75"
        >  <Parallaxy
                  axis="x"
                  :speed="-100"
                  :breakpoints="{ 3024: { axis: 'x', speed: -100 } }"
                
                >
          <span>
            P3 Enterprise believes in the power of unforgettable moments. Our passion lies in
            crafting extraordinary experiences that leave a lasting impression on our clients and
            their guests.
          </span>
        </Parallaxy>
        </h1>
        <div class="box relative grid gap-6 col-span-2 row-span-3 lg:w-1/2 justify-center">
            <div class="col-start-2 row-span-2">

                <Parallaxy
                  axis="y"
                  :speed="-200"
                  :breakpoints="{ 3024: { axis: 'y', speed: -200 } }"
                  
                >
                <div
                class="imgBx group  relative w-[150px] h-[250px] overflow-hidden shadow-xl jarallax transition-all duration-500 delay-100"
                >
                <img
                    class="absolute top-0 left-0 w-full h-full object-cover jarallax-image rotate-12 scale-150 transition-transform delay-75 ease-in-out duration-500 group-hover:rotate-0 group-hover:scale-100"
                    src="../assets/images/wedding.jpg"
                    alt=""
                    />
                </div>
            </Parallaxy>
            
        </div>
        <div class="col-start-1 row-start-2 row-span-2">
            <Parallaxy
              axis="y"
              :speed="200"           
            >
            <div
            class="imgBx group  relative w-[150px] h-[250px] overflow-hidden shadow-xl jarallax transition-all duration-500"
            >
            <img
            class="absolute top-0 left-0 w-full h-full object-cover jarallax-image rotate-12 scale-150 transition-transform delay-75 ease-in-out duration-500 group-hover:rotate-0 group-hover:scale-100"
            src="../assets/images/wedding2.jpg"
            alt=""
            />
        </div>
    </Parallaxy>
        </div>
        </div>
      </div>
      <div v-motion-slide-visible-right :delay="300" class="flex flex-col lg:flex-row-reverse py-6 items-center lg:gap-6">
        <h1
        class="hover-3 leading-10 text-right mb-6 md:text-2xl lg:w-1/2 text-white text-2xl font-bold capitalize transition-all delay-75"
        >
        <Parallaxy
                  axis="x"
                  :speed="100"
                > 
          <span
            >With over a decade of experience in the event planning industry, we have honed our
            skills to perfection, ensuring seamless execution and attention to every detail. From
            intimate gatherings to lavish celebrations, we approach each event with creativity,
            innovation, and a personalized touch.
          </span>
        </Parallaxy>
        </h1> 
        <div class="box relative grid gap-6 col-span-2 row-span-3 lg:w-1/2 justify-center">
            <div class="col-start-1 row-span-2 ">
    
           
                <Parallaxy
                  axis="y"
                  :speed="-200"
                  :breakpoints="{ 2024: { axis: 'y', speed: -200 } }"
                  
                >
          <div
            class="imgBx group relative w-[150px] h-[250px] overflow-hidden shadow-xl jarallax transition-all duration-500 delay-100"
          >
            <img
              class="absolute top-0 left-0 w-full h-full object-cover jarallax-image rotate-12 scale-150 transition-transform delay-75 ease-in-out duration-500 group-hover:rotate-0 group-hover:scale-100"
              src="../assets/images/wedding4.jpg"
              alt=""
            />
          </div></Parallaxy> </div>
          <div class="col-start-2 row-start-2 row-span-2">
            <Parallaxy
                  axis="y"
                  :speed="200"
                  :breakpoints="{ 2024: { axis: 'y', speed: -200 } }"
                  
                >
              <div
                class="imgBx group  relative w-[150px] h-[250px] overflow-hidden shadow-xl jarallax transition-all duration-500"
              >
                <img
                  class="absolute top-0 left-0 w-full h-full object-cover jarallax-image rotate-12 scale-150 transition-transform delay-75 ease-in-out duration-500 group-hover:rotate-0 group-hover:scale-100"
                  src="../assets/images/birthday3.jpg"
                  alt=""
                />
              </div>
            </Parallaxy>
          </div>
        </div>
      </div>
        <div v-motion-slide-visible-left :delay="300" class="flex  flex-col lg:flex-row items-center pt-12 lg:gap-6">
      
        <h1
          data-jarallax-element="0 -200"
          class="hover-3 leading-10 text-left mb-6 md:text-2xl lg:w-1/2 text-white text-2xl font-bold capitalize transition-all delay-75"
        >  <Parallaxy
                  axis="x"
                  :speed="-100"
                  :breakpoints="{ 3024: { axis: 'x', speed: -100 } }"
                
                >
          <span>
            P3 Enterprise believes in the power of unforgettable moments. Our passion lies in
            crafting extraordinary experiences that leave a lasting impression on our clients and
            their guests.
          </span>
        </Parallaxy>
        </h1>
        <div class="box relative grid gap-6 col-span-2 row-span-3 lg:w-1/2 justify-center">
            <div class="col-start-2 row-span-2">

                <Parallaxy
                  axis="y"
                  :speed="-200"
                  :breakpoints="{ 3024: { axis: 'y', speed: -200 } }"
                  
                >
                <div
                class="imgBx group  relative w-[150px] h-[250px] overflow-hidden shadow-xl jarallax transition-all duration-500 delay-100"
                >
                <img
                    class="absolute top-0 left-0 w-full h-full object-cover jarallax-image rotate-12 scale-150 transition-transform delay-75 ease-in-out duration-500 group-hover:rotate-0 group-hover:scale-100"
                    src="../assets/images/wedding3.jpg"
                    alt=""
                    />
                </div>
            </Parallaxy>
            
        </div>
        <div class="col-start-1 row-start-2 row-span-2">
            <Parallaxy
              axis="y"
              :speed="200"           
            >
            <div
            class="imgBx group  relative w-[150px] h-[250px] overflow-hidden shadow-xl jarallax transition-all duration-500"
            >
            <img
            class="absolute top-0 left-0 w-full h-full object-cover jarallax-image rotate-12 scale-150 transition-transform delay-75 ease-in-out duration-500 group-hover:rotate-0 group-hover:scale-100"
            src="../assets/images/weddingrings.jpeg"
            alt=""
            />
        </div>
    </Parallaxy>
        </div>
        </div>
      </div>
      <div v-motion-slide-visible-right :delay="300" class="flex flex-col lg:flex-row-reverse py-6 items-center lg:gap-6">
        <h1
        class="hover-3 leading-10 text-right mb-6 md:text-2xl lg:w-1/2 text-white text-2xl font-bold capitalize transition-all delay-75"
        >
        <Parallaxy
                  axis="x"
                  :speed="100"
                > 
          <span
            >With over a decade of experience in the event planning industry, we have honed our
            skills to perfection, ensuring seamless execution and attention to every detail. From
            intimate gatherings to lavish celebrations, we approach each event with creativity,
            innovation, and a personalized touch.
          </span>
        </Parallaxy>
        </h1> 
        <div class="box relative grid gap-6 col-span-2 row-span-3 lg:w-1/2 justify-center">
            <div class="col-start-1 row-span-2 ">
    
           
                <Parallaxy
                  axis="y"
                  :speed="-200"
                  :breakpoints="{ 2024: { axis: 'y', speed: -200 } }"
                  
                >
          <div
            class="imgBx group relative w-[150px] h-[250px] overflow-hidden shadow-xl jarallax transition-all duration-500 delay-100"
          >
            <img
              class="absolute top-0 left-0 w-full h-full object-cover jarallax-image rotate-12 scale-150 transition-transform delay-75 ease-in-out duration-500 group-hover:rotate-0 group-hover:scale-100"
              src="../assets/images/Venue.jpeg"
              alt=""
            />
          </div></Parallaxy> </div>
          <div class="col-start-2 row-start-2 row-span-2">
            <Parallaxy
                  axis="y"
                  :speed="200"
                  :breakpoints="{ 2024: { axis: 'y', speed: -200 } }"
                  
                >
              <div
                class="imgBx group  relative w-[150px] h-[250px] overflow-hidden shadow-xl jarallax transition-all duration-500"
              >
                <img
                  class="absolute top-0 left-0 w-full h-full object-cover jarallax-image rotate-12 scale-150 transition-transform delay-75 ease-in-out duration-500 group-hover:rotate-0 group-hover:scale-100"
                  src="../assets/images/anniversary.jpg"
                  alt=""
                />
              </div>
            </Parallaxy>
          </div>
        </div>
      </div>
     
    </div>
  </section>
</template>
<script setup>
// import WorksPhone from './WorksPhone.vue'
import Parallaxy from '@lucien144/vue3-parallaxy'
</script>

<script>
export default {
  data() {
    return {
      translateX: 50
    }
  },
  mounted() {
    window.addEventListener('scroll', this.handleScroll)
  },
  beforeUnmount() {
    // Remove scroll event listener to avoid memory leaks
    window.removeEventListener('scroll', this.handleScroll)
  },
  methods: {
    handleScroll() {
      // Calculate the new translateY value based on scroll position
      const scrollTop = window.scrollY
      this.translateX = -scrollTop / 5
    //   console.log(this.translateX)
      // Adjust the multiplier for desired parallax effect
    }
  }
}
</script>

<!-- <script>
export default {
  data() {
    return {
       
      translateX: 0
    }
  },
  mounted() {
    // Listen for scroll events
    document.addEventListener("mousemove", this.parallax);
    window.addEventListener('scroll', this.handleScroll)
  },
  beforeUnmount() {
      // Remove scroll event listener to avoid memory leaks
      document.removeEventListener("mousemove", this.parallax);
    window.removeEventListener('scroll', this.handleScroll)
  },
  methods: {
    handleScroll() {
      // Calculate the new translateY value based on scroll position
      const scrollTop = window.scrollY
      this.translateX = scrollTop / 1.5
      console.log(this.translateX);
      // Adjust the multiplier for desired parallax effect
    } ,
    parallax(e) {
      const layers = document.querySelectorAll(".layer");
      layers.forEach((layer) => {
        const speed = layer.getAttribute("data-speed");
        const x = (window.innerWidth - e.pageX * speed) / 100;
        const y = (window.innerHeight - e.pageY * speed) / 100;
        layer.style.transform = `translateX(${x}px) translateY(${y}px)`;
      });
    }
  }
}
</script> -->

<style scoped>
.circular {
  /* font-size: 1em; */
  animation: animate 7.5s linear infinite;
}

@keyframes animate {
  0% {
    transform: rotate(360deg);
    color: #ff521b;
  }
  100% {
    transform: rotate(0deg);
  }
}

section .circular span {
  position: absolute;
  top: -100;
  left: -100;
  text-transform: uppercase;
  display: inline-block;
  transform-origin: 0 70px;
}
.hover-3 {
  --b: 0.1em; /* the thickness of the line */
  --c: #93032e; /* the color */

  color: #fff;
  padding-block: var(--b);
  background:
    linear-gradient(var(--c) 50%, #fff 0) 0% calc(100% - var(--_p, 0%)) / 100% 200%,
    linear-gradient(var(--c) 0 0) 0% var(--_p, 0%) / var(--_p, 0%) var(--b) no-repeat;
  -webkit-background-clip: text, padding-box;
  background-clip: text, padding-box;
  transition:
    0.5s var(--_s, 0s) linear,
    background-size 0.3s calc(0.3s - var(--_s, 0s));
}
.hover-3:hover {
  --_p: 100%;
  --_s: 0.3s;
  color: var(--c);
}
</style>
