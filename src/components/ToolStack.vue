<template>
  <section class="z-30 bg-green relative overflow-hidden py-12 lg:pt-20 min-h-screen">
    <div
      class="container m-auto lg:py-3 bg-transparent flex flex-col lg:flex-row justify-center items-center"
    >
      <div class="w-full relative">
        <div class="flex m-auto justify-center items-center">
          <div v-motion-slide-visible-top :delay="300" class="flex m-auto">
            <Parallaxy axis="x" :speed="300" :breakpoints="{ 3024: { axis: 'x', speed: 300 } }">
            </Parallaxy>
          </div>
        </div>
      </div>
      <div class="w-full lg:w-4/12 relative"></div>
    </div>
    <div class="container relative m-auto px-5">
      <article class="wrapper">
        <div class="marquee">
          <div class="marquee__group">
            <h1
              data-replace="Tools Stack."
              role="heading"
              class="sticky text-white text-center worksheader whitespace-nowrap w-full leading-10 pb-4 lg:text-6xl md:text-5xl text-3xl font-bold capitalize transition-all"
            >
              <span>Hear the Joy We Create. Personalized Birthday Songs for Delighted Clients. Discover how we can make someone's day extra special.</span>
            </h1>
          </div>
          <div class="marquee__group">
            <h1
              data-replace="Tools Stack."
              role="heading"
              class="sticky text-white text-center worksheader whitespace-nowrap w-full leading-10 pb-4 lg:text-6xl md:text-5xl text-3xl font-bold capitalize transition-all"
            >
              <span>Hear the Joy We Create. Personalized Birthday Songs for Delighted Clients. Discover how we can make someone's day extra special.</span>
            </h1>
          </div>
        </div>
        <div class="marquee marquee--reverse">
          <MarqueeGroup />

          <MarqueeGroup />
        </div>
      </article>
    </div>
  </section>
</template>
<script setup>
import MarqueeGroup from './MarqueeGroup.vue'

import Parallaxy from '@lucien144/vue3-parallaxy'
</script>

<style>
/* 3d animation */
/* .card:hover .box {
        transform: rotateY(180deg);
    } */
:root {
  --color-text: navy;
  --color-bg: papayawhip;
  --color-bg-accent: #1b1b3a;
  --size: clamp(7rem, 1rem + 40vmin, 30rem);
  --gap: calc(var(--size) / 10);
  --duration: 60s;
  --scroll-start: 0;
  --scroll-end: calc(-100% - var(--gap));
}

.marquee {
  display: flex;
  overflow: hidden;
  user-select: none;
  gap: var(--gap);
  mask-image: linear-gradient(
    var(--mask-direction, to right),
    hsl(0 0% 0% / 0),
    hsl(0 0% 0% / 1) 20%,
    hsl(0 0% 0% / 1) 80%,
    hsl(0 0% 0% / 0)
  );
}

.marquee__group {
  flex-shrink: 0;
  display: flex;
  align-items: center;
  justify-content: space-around;
  gap: var(--gap);
  min-width: 100%;
  animation: scroll-x var(--duration) linear infinite;
}

@media (prefers-reduced-motion: reduce) {
  .marquee__group {
    animation-play-state: paused;
  }
}

.marquee--reverse .marquee__group {
  animation-direction: reverse;
  animation-delay: -3s;
}

@keyframes scroll-x {
  from {
    transform: translateX(var(--scroll-start));
  }

  to {
    transform: translateX(var(--scroll-end));
  }
}

/* Element styles */

/* Parent wrapper */
.wrapper {
  display: flex;
  flex-direction: column;
  gap: var(--gap);
  margin: auto;
  max-width: 100vw;
}

/* Toggle direction button */
.toggle {
  --size: 3rem;
  position: relative;
  position: fixed;
  top: 1rem;
  left: 1rem;
  width: var(--size);
  height: var(--size);
  font: inherit;
  text-align: center;
  cursor: pointer;
  outline: none;
  border: none;
  border-radius: 50%;
  color: inherit;
  background-color: var(--color-bg-accent);
  z-index: 1;
}

.toggle:focus-visible {
  box-shadow: 0 0 0 2px var(--color-text);
}

.toggle span {
  position: absolute;
  display: inline-block;
  top: 50%;
  left: calc(100% + 0.4em);
  width: fit-content;
  white-space: nowrap;
  transform: translateY(-50%);
  animation: fade 400ms 4s ease-out forwards;
  user-select: none;
}

/* Element styles */
.marquee img {
  display: grid;
  place-items: center;
  width: 250px;
  height: 150px;
  fill: var(--color-text);
  background: var(--color-bg-accent);
  aspect-ratio: 16/9;
  padding: calc(var(--size) / 10) calc(var(--size) / 5);
  border-radius: 0.5rem;
}

/* Parent wrapper */
.wrapper {
  display: flex;
  flex-direction: column;
  gap: var(--gap);
  margin: auto;
  max-width: 100vw;
}

/* Toggle direction button */
.toggle {
  --size: 3rem;
  position: relative;
  position: fixed;
  top: 1rem;
  left: 1rem;
  width: var(--size);
  height: var(--size);
  font: inherit;
  text-align: center;
  cursor: pointer;
  outline: none;
  border: none;
  border-radius: 50%;
  color: inherit;
  background-color: var(--color-bg-accent);
  z-index: 1;
}

.toggle:focus-visible {
  box-shadow: 0 0 0 2px var(--color-text);
}

.toggle span {
  position: absolute;
  display: inline-block;
  top: 50%;
  left: calc(100% + 0.4em);
  width: fit-content;
  white-space: nowrap;
  transform: translateY(-50%);
  animation: fade 400ms 4s ease-out forwards;
  user-select: none;
}

.toggle img {
  --size: 1.5rem;
  position: absolute;
  top: 50%;
  left: 50%;
  width: var(--size);
  height: var(--size);
  fill: currentcolor;
  transform: translate(-50%, -50%);
  transition: transform 300ms cubic-bezier(0.25, 1, 0.5, 1);
}

@keyframes fade {
  to {
    opacity: 0;
    visibility: hidden;
  }
}
</style>
