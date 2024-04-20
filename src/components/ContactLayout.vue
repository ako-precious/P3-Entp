
<template>
    <!-- <Parallaxy :speed="20" :animation="(delta: number) => `transform: translate3d(0, ${delta}px, 0);`"> -->
		
        <section class="z-0 relative overflow-hidden py-12 min-h-screen" id="contact" >
        <div class="fixed w-full h-full bottom-0"> 

            <div
                class=" container m-auto lg:py-6 bg-transparent flex justify-center items-center"
            >
                <div  v-motion-slide-visible-bottom :delay="200"
                    class="m-auto w-full md:w-7/12 flex bg-darkblue p-6 flex-col-reverse lg:flex-row justify-center items-center shadow-xl rounded-xl"
                >
                    <slot></slot>
                </div>
            </div>
        </div>
        </section>
	<!-- </Parallaxy> -->
</template>
<script setup lang="ts">
// import Parallaxy from '@lucien144/vue3-parallaxy';
</script>