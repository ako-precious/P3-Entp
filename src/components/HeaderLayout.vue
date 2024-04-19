<template>
  <header
    class="m-auto fixed w-full top-0 flex justify-between p-3 lg:px-12 items-center z-50 transition-all"
  >
    <div class="dropdown group bg-gray-600 bg-clip-padding backdrop-filter backdrop-blur-xl bg-opacity-20 rounded-3xl text-red button">
      <input type="checkbox" id="dropdown" />
      <label
        class="dropdown__face rounded-md cursor-pointer"
        for="dropdown"
      >
        <div class="dropdown__text text-lg sm:text-xl group-hover:text-darkblue h-6 font-semibold">
          <span class="span-mother flex overflow-hidden">
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

        <div class="dropdown__arrow text-red"></div>
      </label>
      <ul class="dropdown__items text-lg">
        <li>🙂</li>
        <li>😺</li>
        <li>😽</li>
        <li>😎</li>
        <li class="hover:text-darkblue"><a href="#contact">Contact</a></li>
      </ul>
    </div>

    <svg>
      <filter id="goo">
        <feGaussianBlur in="SourceGraphic" stdDeviation="10" result="blur" />
        <feColorMatrix
          in="blur"
          type="matrix"
          values="1 0 0 0 0  0 1 0 0 0  0 0 1 0 0  0 0 0 18 -7"
          result="goo"
        />
        <feBlend in="SourceGraphic" in2="goo" />
      </filter>
    </svg>

    <h1
      class="logo text-xl sm:text-2xl md:text-3xl p-3 mr-4 whitespace-nowrap tracking-widest font-black text-red z-10"
    >
      <a href="#"> P3 Enterprise</a>
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
<style>
.dropdown {
  position: relative;
  width: 110px;
  filter: url(#goo);
}

.dropdown__face,
.dropdown__items {
  padding: 15px;
  display: flex;
  flex-direction: column;
  border-radius: 25px;
}

.dropdown__face:hover,
.dropdown__items {
  background: white;
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
  content: '';
  background-color: #fff;
  position: absolute;
  bottom: 100%;
  right: 20%;
  height: 40px;
  width: 20px;
}

.dropdown__arrow {
  border-bottom: 2px solid #93032e;
  border-right: 2px solid #93032e;
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
input:checked ~ .dropdown__face {
  background: white;
}

svg {
  display: none;
}

.button:hover .span-mother {
  position: absolute;
}

.button:hover .span-mother span {
  transform: translateY(1.3em);
}

.button .span-mother span:nth-child(1) {
  transition: 0.2s;
}

.button .span-mother span:nth-child(2) {
  transition: 0.3s;
}

.button .span-mother span:nth-child(3) {
  transition: 0.4s;
}

.button .span-mother span:nth-child(4) {
  transition: 0.5s;
}

.button .span-mother span:nth-child(5) {
  transition: 0.6s;
}

.button .span-mother span:nth-child(6) {
  transition: 0.7s;
}
.button .span-mother2 {
  display: flex;
  position: absolute;
  overflow: hidden;
}

.button .span-mother2 span {
  transform: translateY(-1.5em);
}

.button:hover .span-mother2 span {
  transform: translateY(0);
}

.button .span-mother2 span {
  transition: 0.2s;
}

.button .span-mother2 span:nth-child(2) {
  transition: 0.3s;
}

.button .span-mother2 span:nth-child(3) {
  transition: 0.4s;
}

.button .span-mother2 span:nth-child(4) {
  transition: 0.5s;
}

.button .span-mother2 span:nth-child(5) {
  transition: 0.6s;
}

.button .span-mother2 span:nth-child(6) {
  transition: 0.7s;
}
</style>
