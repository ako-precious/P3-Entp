<template>
  <MainLayout>
    <Introduction />
  </MainLayout>
  <NewParallax />
  <Works />
  
  
  <Contact >
    <Message  />
  </Contact>
  <!-- <ToolStack class="" /> -->
  <!-- <Parallaxy
  axis="y"
  :speed="-200"
  :breakpoints="{ 3024: { axis: 'y', speed: -300 } }"
  class="z-30"
  >
</Parallaxy> -->
</template>

<script setup>
import Contact from '../components/ContactLayout.vue'
import Introduction from '../components/IntroductionLayout.vue'
import NewParallax from '../components/NewParallex.vue'
import MainLayout from '../components/BannerLayout.vue'
import Message from '../components/contact/Message.vue'
// import ToolStack from '../components/ToolStack.vue'
import Works from '../components/WorksLayout.vue'
// import Parallaxy from '@lucien144/vue3-parallaxy'
</script>
