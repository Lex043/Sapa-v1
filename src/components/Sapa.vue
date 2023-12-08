<template>
    <section class="bg-[#FAFBFC] pt-12" ref="sapa_container">
        <div
            class="flex flex-col gap-3 px-2 md:flex-row md:items-center md:gap-4 lg:w-[80%] lg:mx-auto"
        >
            <div class="flex flex-col gap-3 lg:max-w-[32rem] overflow-hidden">
                <h1 class="text-4xl font-bold" data-splitting ref="sapa_title">
                    Sapa<sup>2</sup> nice one nice one
                </h1>
                <p
                    class="text-[1rem] text-[#5F6D7E]"
                    data-splitting
                    ref="sapa_subtitle"
                >
                    Sapa is a state of Ahh God abeg, who we offend, nothing is
                    too small to save a life.
                </p>
                <ul>
                    <li
                        class="flex items-center gap-1 text-[#5F6D7E]"
                        ref="urgent_tukay"
                    >
                        <span><img src="../assets/tick.svg" alt="tick" /></span>
                        <span> Urgent tukay</span>
                    </li>
                    <li
                        class="flex items-center gap-1 text-[#5F6D7E]"
                        ref="garri"
                    >
                        <span><img src="../assets/tick.svg" alt="tick" /></span>
                        <span>Garri</span>
                    </li>
                    <li
                        class="flex items-center gap-1 text-[#5F6D7E]"
                        ref="drop_location"
                    >
                        <span><img src="../assets/tick.svg" alt="tick" /></span>
                        <span>Drop location</span>
                    </li>
                </ul>
                <button
                    class="bg-[#215056] text-white py-2 px-2 w-fit rounded-md flex gap-1 items-center"
                    ref="donate_now"
                >
                    Donate now
                    <span
                        ><img
                            src="../assets/pleading-face.svg"
                            alt="pleading face"
                    /></span>
                </button>
            </div>
            <figure>
                <img src="../assets/sapaImg.png" alt="sapa" />
            </figure>
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

const sapa_container = ref(null);
const sapa_title = ref(null);
const sapa_subtitle = ref(null);
const urgent_tukay = ref(null);
const garri = ref(null);
const drop_location = ref(null);
const donate_now = ref(null);

onMounted(() => {
    Splitting();

    const chars = sapa_title.value.querySelectorAll(".char");
    const chars2 = sapa_subtitle.value.querySelectorAll(".char");

    const tl = gsap.timeline({
        scrollTrigger: {
            trigger: sapa_container.value,
            start: "top center",
            once: true,
        },
    });

    tl.from(chars, {
        opacity: 0,
        duration: 1,
        stagger: 0.05,
        ease: "power2.inOut",
    });

    tl.from(
        chars2,
        {
            opacity: 0,
            duration: 0.2,
            stagger: 0.02,
            ease: "power2.inOut",
        },
        "<"
    );

    tl.fromTo(urgent_tukay.value, { opacity: 0, y: 100 }, { opacity: 1, y: 0 });

    tl.fromTo(garri.value, { opacity: 0, y: 100 }, { opacity: 1, y: 0 });

    tl.fromTo(
        drop_location.value,
        { opacity: 0, y: 100 },
        { opacity: 1, y: 0 }
    );

    tl.fromTo(donate_now.value, { opacity: 0, y: 100 }, { opacity: 1, y: 0 });
});
</script>
