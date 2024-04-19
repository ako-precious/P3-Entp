<template>
    <div
        class="container m-auto bg-transparent flex flex-col lg:flex-row justify-center items-center"
    >
        <div class="w-full lg:w-6/12 py-6 relative written-text">
            <div class="flex w-64 md:w-96 m-auto flex-col justify-center">
                <h1
                    data-replace="Full-Stack developer."
                    role="heading"
                    class="swap leading-10 pb-4 lg:text-7xl md:text-5xl text-darkblue text-3xl font-bold capitalize transition-all delay-75"
                >
                    <span
                        >Full-Stack <br />
                        developer.
                    </span>
                </h1>
                <p
                    ref="text"
                    class="texts pb-4 text-white text-base"
                    v-html="formattedText"
                ></p>
            </div>
        </div>
        <div class="w-full lg:w-6/12 pt-3 m-auto relative my-image">
            <div
                class="outer w-64 md:w-80 h-64 md:h-80 m-auto grid place-items-center layer"
                data-speed="0"
            >
            <svg class=" absolute w-full h-full object-cover"   viewBox="0 0 200 200" xmlns="http://www.w3.org/2000/svg">
  <path fill="#FF0066" d="M42.1,-39.7C53.8,-30.5,61.9,-15.2,60.5,-1.4C59.2,12.5,48.4,25.1,36.7,38.9C25.1,52.8,12.5,68,1,66.9C-10.5,65.9,-21,48.7,-37.1,34.9C-53.2,21,-74.9,10.5,-80.2,-5.3C-85.5,-21.1,-74.4,-42.2,-58.3,-51.4C-42.2,-60.6,-21.1,-58,-2.9,-55.1C15.2,-52.2,30.5,-49,42.1,-39.7Z" transform="translate(100 100)" />
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
                "I, as a full stack developer, can provide the technical expertise and creative solutions necessary to build a website that stands out by reflecting how you want the world to see you...", // Replace with your text
            letters: [],
        };
    },
    computed: {
        formattedText() {
            return this.originalText.replace(
                /\S/g,
                '<span class="smoke">$&</span>'
            );
        },
    },
    mounted() {
        this.letters = this.$refs.text.querySelectorAll(".smoke");
        this.attachHoverListeners();
    },
    methods: {
        attachHoverListeners() {
            this.letters.forEach((letter) => {
                letter.addEventListener("mouseover", () => {
                    letter.classList.toggle("active");
                });
            });
        },
    },
};
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
