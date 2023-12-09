<template>
    <section class="bg-[#FAFBFC] py-10" ref="donate_container">
        <div class="flex flex-col gap-3 px-2 lg:w-[80%] lg:mx-auto">
            <div class="flex flex-col gap-4">
                <h1
                    class="text-[#272D37] text-[2rem] text-center font-semibold lg:max-w-[50rem] lg:mx-auto"
                    data-splitting
                    ref="donate_title"
                >
                    We are happy to have you here, thanks for being there always
                    .
                </h1>
                <form action="submit" class="flex justify-center">
                    <input
                        type="text"
                        placeholder="Our account number"
                        class="border-[1px] pl-2 w-full md:w-[25rem] rounded-md"
                    />

                    <button
                        class="bg-[#215056] text-white text-sm py-2 px-2 w-[13rem] md:w-[8rem] rounded-md flex gap-1 items-center justify-center"
                    >
                        Donate now
                        <span
                            ><img
                                src="../assets/pleading-face.svg"
                                alt="pleading face"
                        /></span>
                    </button>
                </form>
                <div class="flex flex-wrap gap-3 justify-center">
                    <p class="flex items-center gap-1 text-[#272D37] text-base">
                        <span
                            ><img src="../assets/circle-tick.svg" alt=""
                        /></span>
                        Fully Secure
                    </p>

                    <p class="flex items-center gap-1 text-[#272D37] text-base">
                        <span
                            ><img src="../assets/circle-tick.svg" alt=""
                        /></span>
                        24/7 Support
                    </p>

                    <p class="flex items-center gap-1 text-[#272D37] text-base">
                        <span
                            ><img src="../assets/circle-tick.svg" alt=""
                        /></span>
                        Done Deal
                    </p>
                </div>
            </div>
        </div>
    </section>
</template>

<script setup>
import gsap from "gsap";
import Splitting from "splitting";
import "splitting/dist/splitting.css";
import { ScrollTrigger } from "gsap/ScrollTrigger";
import { onMounted, ref } from "vue";
gsap.registerPlugin(ScrollTrigger);

const donate_container = ref(null);
const donate_title = ref(null);

onMounted(() => {
    Splitting();

    const chars = donate_title.value.querySelectorAll(".char");

    const tl = gsap.timeline({
        scrollTrigger: {
            trigger: donate_container.value,
            start: "top center+=200",
            once: true,
        },
    });

    tl.from(chars, {
        opacity: 0,
        duration: 1,
        stagger: 0.05,
        ease: "power2.inOut",
    });
});
</script>
