<template>
  <div class="parallax-container" ref="parallaxContainer">
    <div class="parallax-section" :style="{ transform: `translateY(${translateY}px)` }">
      <!-- Content of the parallax section -->
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
       
      translateY: 0
    }
  },
  mounted() {
    // Listen for scroll events
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
      this.translateY = scrollTop * 0.5 // Adjust the multiplier for desired parallax effect
    }
  }
}
</script>

<style scoped>
.parallax-container {
  overflow: hidden;
  position: relative;
  height: 100vh; /* Adjust height as needed */
}

.parallax-section {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background-image: url('/src/assets/images/Àdúrà òbí 🤍_ Yorùbá Wedding.jpeg');
  background-size: cover;
  background-position: center;
}
</style>
