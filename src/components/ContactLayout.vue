
<template>
    <section class="relative bg-green overflow-hidden py-12 min-h-screen" id="contact" >
    
        <div
            class="container m-auto lg:py-6 bg-transparent flex justify-center items-center"
        >
            <div v-motion-roll-visible-left :delay="200"
                class="m-auto w-full md:w-7/12 flex bg-darkblue p-6 flex-col-reverse lg:flex-row justify-center items-center shadow-xl rounded-xl"
            >
                <slot></slot>
            </div>
        </div>
    </section>
</template>
<script setup >


</script>