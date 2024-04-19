<template>
  <MainLayout class=" ">
    <Fullstack />
  </MainLayout>
  <Works />

  <NewParallex />

  <img src="https://picsum.photos/500" />
  <ToolStack class="" />
  <Parallaxy
    axis="y"
    :speed="-200"
    :breakpoints="{ 3024: { axis: 'y', speed: -300 } }"
    class="self-center z-30"
  >
</Parallaxy>
    <Contact >
      <Message  />
    </Contact>
</template>

<script setup>
import Contact from '../components/ContactLayout.vue'
import Fullstack from '../components/FullStack.vue'
import NewParallex from '../components/NewParallex.vue'
import MainLayout from '../components/BannerLayout.vue'
import Message from '../components/contact/Message.vue'
import ToolStack from '../components/ToolStack.vue'
import Works from '../components/WorksLayout.vue'
import Parallaxy from '@lucien144/vue3-parallaxy'
</script>
