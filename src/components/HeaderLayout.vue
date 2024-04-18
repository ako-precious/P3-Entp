<template>
  <header 
    class="   m-auto  fixed w-full top-0 flex justify-between p-3  lg:px-12 items-center z-50 transition-all"
  >
    <div class="p-3 card flex justify-center">
      
      
      <button class="  dark:text-white text-black shadow-extra-small rounded-md cursor-pointer w-[50px] h-[20px] text-oynx dark:text-snow font-semibold border-none flex justify-center items-center">
                                        <span
                                            class="span-mother flex overflow-hidden">
                                            <span>M</span>
                                            <span>e</span>
                                            <span>n</span>
                                            <span>u</span>  
                                        </span>
                                        <span class="span-mother2 text-persian">
                                            <span>M</span>
                                            <span>e</span>
                                            <span>n</span>
                                            <span>u</span>
                                        </span>
                                        </button>
    </div>
    <div class="dropdown">
  <input type="checkbox" id="dropdown">
<button class=" text-black shadow-extra-small rounded-md cursor-pointer w-[150px] h-[20px] text-oynx dark:text-snow font-semibold border-none flex justify-center items-center">
  <label class="dropdown__face" for="dropdown">
    <div class="dropdown__text">  
                                        <span
                                            class="span-mother flex overflow-hidden">
                                            <span>M</span>
                                            <span>e</span>
                                            <span>n</span>
                                            <span>u</span>  
                                        </span>
                                        <span class="span-mother2 text-persian">
                                            <span>M</span>
                                            <span>e</span>
                                            <span>n</span>
                                            <span>u</span>
                                        </span>
                                        </div>

    <div class="dropdown__arrow"></div>
  </label>
</button>
  <ul class="dropdown__items">
    <li>🙂</li>
    <li>😺</li>
    <li>😽</li>
    <li>😎</li>
    <li>🤗</li>
  </ul>
</div>

<svg>
  <filter id="goo">
    <feGaussianBlur in="SourceGraphic" stdDeviation="10" result="blur" />
    <feColorMatrix in="blur" type="matrix" values="1 0 0 0 0  0 1 0 0 0  0 0 1 0 0  0 0 0 18 -7" result="goo" />
    <feBlend in="SourceGraphic" in2="goo" />
  </filter>
</svg>
    <!-- <svg viewBox="0 0 200 200" xmlns="http://www.w3.org/2000/svg">
  <path fill="#FF0066" d="M42.1,-39.7C53.8,-30.5,61.9,-15.2,60.5,-1.4C59.2,12.5,48.4,25.1,36.7,38.9C25.1,52.8,12.5,68,1,66.9C-10.5,65.9,-21,48.7,-37.1,34.9C-53.2,21,-74.9,10.5,-80.2,-5.3C-85.5,-21.1,-74.4,-42.2,-58.3,-51.4C-42.2,-60.6,-21.1,-58,-2.9,-55.1C15.2,-52.2,30.5,-49,42.1,-39.7Z" transform="translate(100 100)" />
</svg> -->
    <h1
      class="jacquard-24-regular text-3xl  p-3 mr-4 whitespace-nowrap tracking-widest font-black dark:text-white text-black z-10 "
      
    >
      P3 Enterprise
    </h1>
  </header>
</template>

<script>
// Creating a smoke animation
export default {
  inheritAttrs: false,
 
  methods: {
   
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
<style >

.dropdown {
  position: relative;
  width: 100px;
  filter: url(#goo);
}

.dropdown__face,
.dropdown__items {
  background-color: #fff;
  padding: 20px;
  display: flex;
  flex-direction: column;
  border-radius: 25px;
}

.dropdown__face {
  display: block;
  position: relative;
}

.dropdown__items {
  margin: 0;
  position: absolute;
  right: 0;
  top: 50%;
  width: 100%;
  list-style: none;
  display: flex;
  justify-content: space-between;
  visibility: hidden;
  z-index: -1;
  opacity: 0;
  transition: all 0.4s cubic-bezier(0.93, 0.88, 0.1, 0.8);
}

.dropdown__items::before {
  content: "";
  background-color: #fff;
  position: absolute;
  bottom: 100%;
  right: 20%;
  height: 40px;
  width: 20px;
}

.dropdown__arrow {
  border-bottom: 2px solid #000;
  border-right: 2px solid #000;
  position: absolute;
  top: 50%;
  right: 30px;
  width: 10px;
  height: 10px;
  transform: rotate(45deg) translateY(-50%);
  transform-origin: right;
}

input {
  display: none;
}

input:checked ~ .dropdown__items {
  top: calc(100% + 25px);
  visibility: visible;
  opacity: 1;
}

body {
  background-image: linear-gradient(140deg, #e2e2e2, #cdcdcd);
  display: grid;
  place-items: center;
  font-family: "Lato", Arial, sans-serif;
  height: 100vh;
  margin: 0;
}

* {
  box-sizing: border-box;
}

svg {
  display: none;
}





button:hover .span-mother {
    position: absolute;
}

button:hover .span-mother span {
    transform: translateY(1.3em);
}

button .span-mother span:nth-child(1) {
    transition: 0.2s;
}

button .span-mother span:nth-child(2) {
    transition: 0.3s;
}

button .span-mother span:nth-child(3) {
    transition: 0.4s;
}

button .span-mother span:nth-child(4) {
    transition: 0.5s;
}

button .span-mother span:nth-child(5) {
    transition: 0.6s;
}

button .span-mother span:nth-child(6) {
    transition: 0.7s;
}
button .span-mother2 {
    display: flex;
    position: absolute;
    overflow: hidden;
}

button .span-mother2 span {
    transform: translateY(-1.5em);
}

button:hover .span-mother2 span {
    transform: translateY(0);
}

button .span-mother2 span {
    transition: 0.2s;
}

button .span-mother2 span:nth-child(2) {
    transition: 0.3s;
}

button .span-mother2 span:nth-child(3) {
    transition: 0.4s;
}

button .span-mother2 span:nth-child(4) {
    transition: 0.5s;
}

button .span-mother2 span:nth-child(5) {
    transition: 0.6s;
}

button .span-mother2 span:nth-child(6) {
    transition: 0.7s;
}

/* Glassmorphism card effect */
.card {
    backdrop-filter: blur(8px) saturate(200%);
    -webkit-backdrop-filter: blur(8px) saturate(200%);
    background-color: rgba(17, 25, 40, 0.24);
    border-radius: 12px;
    border: 1px solid rgba(255, 255, 255, 0.125);
}

.jacquard-24-regular {
    font-family: "Dancing Script", cursive;
  font-optical-sizing: auto;
  font-weight: 700;
  font-style: normal;
}

</style>
