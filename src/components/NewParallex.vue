<template>
   
    <section
        class="bg-darkblue z-10 min-h-screen banner overflow-hidden relative flex flex-col justify-center items-center
         w-full m-auto py-12 " style="background-image: linear-gradient(140deg, #e2e2e2, #cdcdcd);"> 
        
      <div class="w-full py-6 relative">
        <div v-motion-slide-visible-top :delay="300"  class="flex m-auto">
            <Parallaxy
                  axis="x"
                  :speed="-100"
                  :breakpoints="{ 3024: { axis: 'x', speed: -300 } }"
                
                >
          <h1
            
          role="heading"
          class="sticky text-center worksheader whitespace-nowrap w-full leading-10 pb-4 lg:text-6xl md:text-5xl text-3xl font-bold capitalize transition-all"
          >
          <span>
              What We do</span
              >
            </h1>
        </Parallaxy>
    </div>
    
</div>
<Parallaxy
    axis="y"
    :speed="-100"
    
    > <div v-motion-slide-visible-right :delay="300"  class="container mb-12 card flex flex-col md:flex-row max-w-2xl ">
    <p class="p-4 border-orange border-2 hover:text-white text-orange bg-darkblue group hover:font-sans"><span class="md:rotate-[-90deg]"> <span class="text-xl font-bold ">Birthday Parties</span>  <br> <span class="hidden group-hover:block font-thin text-base  ">Whether it's a milestone birthday or a themed celebration, we know how to make birthdays truly special. Let us take care of the planning, so you can focus on creating cherished memories with your loved ones.</span> </span> </p>
    <p class="p-4 border-orange border-2 hover:text-white text-orange bg-darkblue group hover:font-sans"><span class="md:rotate-[-90deg]"> <span class="text-xl font-bold ">Weddings and Anniversary</span>  <br> <span class="hidden group-hover:block font-thin text-base  ">Let us handle every aspect of your special day, from venue selection and decor to catering and entertainment. We understand the importance of this milestone event and strive to make it unforgettable.</span> </span> </p>
    <p class="p-4 border-orange border-2 hover:text-white text-orange bg-darkblue group hover:font-sans"><span class="md:rotate-[-90deg]"> <span class="text-xl font-bold ">Corporate Events</span>  <br> <span class="hidden group-hover:block font-thin text-base  ">From product launches and conferences to gala dinners and award ceremonies, we have the creativity and resources to plan and execute seamless corporate events that align with your brand's objectives.</span> </span> </p>
    <p class="p-4 border-orange border-2 hover:text-white text-orange bg-darkblue group hover:font-sans"><span class="md:rotate-[-90deg]"> <span class="text-xl font-bold ">Social Gatherings</span>  <br> <span class="hidden group-hover:block font-thin text-base  ">From intimate gatherings with family and friends to large-scale celebrations, we handle events of all sizes with professionalism and creativity. Whatever the occasion, we ensure that every detail is perfect.</span> </span> </p>
    <p class="p-4 border-orange border-2 hover:text-white text-orange bg-darkblue group hover:font-sans"><span class="md:rotate-[-90deg]"> <span class="text-xl font-bold ">Cultural Events</span>  <br> <span class="hidden group-hover:block font-thin text-base  "> Embrace the rich cultural heritage of Nigeria with our expertise in planning traditional ceremonies and cultural celebrations. We respect and honor the traditions and customs that make each event unique.</span> </span> </p>
    
</div>
</Parallaxy>
    </section>
</template>
<script setup>
import Parallaxy from '@lucien144/vue3-parallaxy'
</script>

<style scoped>
.card {
  
  height: 400px;
  border-radius: 4px;
  display: flex;
  gap: 5px;
  padding: .4em;
}

.card p {
  height: 100%;
  flex: 1;
  overflow: hidden;
  cursor: pointer;
  border-radius: 2px;
  transition: all .5s;
  display: flex;
  justify-content: center;
  align-items: center;
}

.card p:hover {
  flex: 4;
}

.card p span {
  min-width: 14em;
  padding: .5em;
  text-align: center;
  letter-spacing: .1em;
}
span{
    transition: all .5s;

}
.card p:hover span {
  transform: rotate(0);
}
</style>
