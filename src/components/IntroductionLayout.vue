<template>
  <div
    class="container m-auto bg-transparent my-16 lg:my-0 flex flex-col lg:flex-row justify-center h-full items-center"
  >
    <div class="w-full lg:w-6/12 py-6 relative written-text">
      <div class="flex w-64 md:w-96 m-auto flex-col justify-center">
        <!-- <h1
                    data-replace="Full-Stack developer."
                    role="heading"
                    class="swap leading-10 pb-4 lg:text-7xl  text-darkblue text-3xl font-bold capitalize transition-all delay-75"
                >
                    <span
                        >Full-Stack <br />
                        developer.
                    </span>
                </h1> -->
        <p
          ref="text"
          class="texts text-xl md:text-3xl pb-4 text-darkblue"
          v-html="formattedText"
        ></p>
      </div>
    </div>
    <div class="w-full lg:w-6/12 pt-3 m-auto relative my-image">
      <div
        class="outer w-64 md:w-80 h-64 md:h-80 m-auto grid place-items-center layer"
        data-speed="0"
      >
        <div class="relative rounded-xl w-[220px] parallax layer"  @mousemove="parallax"  data-speed="-5" >
          <div class="absolute rounded-xl w-full bg-black bg-opacity-80 h-full"></div>
          <div class="absolute -z-10 -m-3 w-full rounded-xl border-2 border-white h-full"></div>
          <div class="absolute -z-10 -m-6 w-full rounded-xl border-2 border-white h-full"></div>

          <video  ref="videoPlayer" class="rounded-xl" width="220" autoplay muted loop>
            <source src="/src/assets/images/wedding.mp4" type="video/mp4" />
            Your browser does not support the video tag.
          </video>
        </div>
        <!-- <iframe src="https://assets.pinterest.com/ext/embed.html?id=767511961522882414" height="520" width="236" frameborder="0" scrolling="no" ></iframe> -->
        <svg viewBox="0 0 200 200" xmlns="http://www.w3.org/2000/svg">
          <path
            fill="#FF0066"
            d="M37.8,-30.1C47.1,-18.4,51.6,-2.8,49.9,14.2C48.3,31.2,40.5,49.6,26.2,57.9C11.8,66.2,-9.2,64.4,-30.7,56.7C-52.2,49,-74.2,35.5,-73.5,21.6C-72.8,7.8,-49.4,-6.4,-33.3,-19.7C-17.3,-32.9,-8.6,-45,2.8,-47.3C14.2,-49.5,28.4,-41.8,37.8,-30.1Z"
            transform="translate(100 100)"
          />
        </svg>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      originalText:
        "Experience the difference with our personalized event planning services. Let's craft something extraordinary together!", // Replace with your text
      letters: []
    }
  },
  computed: {
    formattedText() {
      return this.originalText.replace(/\S/g, '<span class="smoke">$&</span>')
    }
  },
  mounted() {
    this.letters = this.$refs.text.querySelectorAll('.smoke')
    this.attachHoverListeners()

    const video = this.$refs.videoPlayer;
    video.playbackRate = 0.5;

    document.addEventListener('mousemove', this.parallax)
  },
  beforeUnmount() {
    // Remove scroll event listener to avoid memory leaks
    document.removeEventListener('mousemove', this.parallax)
  },
  methods: {
    attachHoverListeners() {
      this.letters.forEach((letter) => {
        letter.addEventListener('mouseover', () => {
          letter.classList.toggle('active')
        })
      })
    },
    parallax(e) {
      const layers = document.querySelectorAll('.layer')
      layers.forEach((layer) => {
        const speed = layer.getAttribute('data-speed')
        const x = (window.innerWidth - e.pageX * speed) / 100
        const y = (window.innerHeight - e.pageY * speed) / 100
        layer.style.transform = `translateX(${x}px) translateY(${y}px)`
      })
    }
  }
}
</script>

<style>
/* smoke animation */
section .texts span {
  position: relative;
  display: inline-block;
  cursor: pointer;
}

section .texts span.active {
  animation: smoke 3s linear forwards;
  transform-origin: bottom;
}

@keyframes smoke {
  0% {
    opacity: 1;
    filter: blur(0);
    transform: translatex(0) translateY(0) rotate(0deg) scale(1);
  }

  50% {
    /* opacity: 1;
                pointer-events: none; */
    opacity: 0;
    filter: blur(20px);
    transform: translatex(300px) translateY(-300px) rotate(740deg) scale(4);
  }

  100% {
    /* opacity: 0;
                filter: blur(20px);
                transform: translatex(300) translateY(-300) rotate(740deg) scale(4); */
    opacity: 1;
    filter: blur(0);
    transform: translatex(0) translateY(0) rotate(0deg) scale(1);
  }
}

/* end of smoke animation */
</style>
