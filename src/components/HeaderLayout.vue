<template>
  <header  :class="{ fix : isHeaderFixed }"
    class="header border-gray-500 bg-gray-200 dark:bg-gray-900  relative top-0 left-0 w-full flex justify-start items-center z-50 py-3 transition-all"
  >
    <div class="ml-6 h-12 w-12">
      <div
        v-on:click="menuOpener()"
        class="marks open group right-0 opacity-0 relative h-12 flex flex-col items-center justify-center w-12 transition-all delay-75 duration-500"
      >
        <div class="bg-white h-1 w-12 z-10"></div>
        <div
          class="bg-white mt-3 mr-4 h-1 w-8 z-10 transition-all delay-75 duration-500 group-hover:mr-0 group-hover:w-12"
        ></div>
      </div>
      <div
        v-on:click="menuCloser()"
        class="marks group close -left-28 -top-full opacity-0 my-auto h-12 w-12 relative z-10 transition-all delay-75 duration-500"
      >
        <div
          class="absolute top-2/4 left-2/4 -translate-y-2/4 -translate-x-2/4 bg-white my-auto rotate-45 mr-6 h-8 w-1 z-10 transition-all delay-75 duration-500 group-hover:h-12"
        ></div>
        <div
          class="absolute top-2/4 left-2/4 -translate-y-2/4 hover:-translate-x-2/4 bg-white my-auto -rotate-45 mr-6 h-6 md:h-12 w-1 z-10"
        ></div>
      </div>
    </div>
    <h1
      class="typing hide absolute top-2/4 left-2/4 -translate-x-2/4 -translate-y-2/4 tracking-widest font-black text-white z-10"
      style="font-size: 3vw"
    >
      P3 Enterprise
    </h1>
  </header>
</template>

<script>
// Creating a smoke animation
export default {
  inheritAttrs: false,
  data() {
        return {
            isHeaderFixed: false,
        };
    },
  beforeDestroy() {
    window.removeEventListener('scroll', this.handleScroll)
  },

  mounted() {
    window.addEventListener('scroll', this.handleScroll)
  },
  methods: {
    handleScroll() {
      // Adjust the scroll threshold as needed
      const scrollThreshold = 20
      this.isHeaderFixed = window.scrollY > scrollThreshold
    },
    menuCloser() {
      document.querySelector('.open').classList.toggle('right-28')
      document.querySelector('.open').classList.toggle('right-0')
      document.querySelector('.close').classList.toggle('left-0')
      document.querySelector('.close').classList.toggle('-left-28')
      document.querySelector('nav').classList.toggle('left-0')
      document.querySelector('nav').classList.toggle('left-[-10000px]')
    },
    menuOpener() {
      document.querySelector('.open').classList.toggle('right-28')
      document.querySelector('.open').classList.toggle('right-0')
      document.querySelector('.close').classList.toggle('left-0')
      document.querySelector('.close').classList.toggle('-left-28')
      document.querySelector('nav').classList.toggle('left-0')
      document.querySelector('nav').classList.toggle('left-[-10000px]')
    }
  }
}
</script>
<style>
.fix  {
    position: fixed;
    top: 0;
    right: 0;
    width: 100%;
    padding: 0.5rem 2rem;
    border-bottom: 1px;
    border-color: rgb(107 114 128 / var(--tw-border-opacity));
    z-index: 1000; /* Adjust z-index as needed */
}</style>