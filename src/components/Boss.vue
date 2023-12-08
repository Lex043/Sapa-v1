<template>
    <section class="bg-[#FAFBFC] py-10" ref="boss_container">
        <div
            class="flex flex-col-reverse gap-3 px-2 md:flex-row md:gap-14 md:items-end lg:w-[80%] lg:mx-auto"
        >
            <figure>
                <img src="../assets/boss.svg" alt="boss" />
                <figcaption
                    class="bg-[#4297AB] text-[#111111] font-semibold text-3xl md:text-5xl text-center rounded-md py-2"
                >
                    I Greet you boss
                </figcaption>
            </figure>
            <div class="flex flex-col gap-3 lg:max-w-[34rem] lg:pb-10">
                <h1
                    data-splitting
                    class="text-4xl font-bold"
                    ref="header_title"
                >
                    Boss I Greet Oh
                </h1>
                <p
                    data-splitting
                    class="text-[1rem] text-[#5F6D7E]"
                    ref="header_subtitle"
                >
                    Help me touch that boss way dey with ehn BF, Boss i greet
                    oh... Na my guy Pablo with them scorpion and croc na ehn
                    send me come meet you, make you give am:
                </p>
                <ul>
                    <li
                        class="flex items-center gap-1 text-[#5F6D7E]"
                        ref="garri"
                    >
                        <span><img src="../assets/tick.svg" alt="tick" /></span>
                        <span>G<sup>2</sup> (Garri and groundnut)</span>
                    </li>
                    <li
                        class="flex items-center gap-1 text-[#5F6D7E]"
                        ref="groccies"
                    >
                        <span><img src="../assets/tick.svg" alt="tick" /></span>
                        <span>Groccies</span>
                    </li>
                    <li
                        class="flex items-center gap-1 text-[#5F6D7E]"
                        ref="cassava_flecks"
                    >
                        <span><img src="../assets/tick.svg" alt="tick" /></span>
                        <span>Cassava flecks</span>
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

const header_title = ref(null);
const boss_container = ref(null);
const header_subtitle = ref(null);
const garri = ref(null);
const groccies = ref(null);
const cassava_flecks = ref(null);
const donate_now = ref(null);

onMounted(() => {
    Splitting();

    const chars = header_title.value.querySelectorAll(".char");
    const chars2 = header_subtitle.value.querySelectorAll(".char");

    const tl = gsap.timeline({
        scrollTrigger: {
            trigger: boss_container.value,
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
            stagger: 0.01,
            ease: "power2.inOut",
        },
        "<40%"
    );

    tl.fromTo(garri.value, { opacity: 0, y: 100 }, { opacity: 1, y: 0 });

    tl.fromTo(groccies.value, { opacity: 0, y: 100 }, { opacity: 1, y: 0 });

    tl.fromTo(
        cassava_flecks.value,
        { opacity: 0, y: 100 },
        { opacity: 1, y: 0 }
    );

    tl.fromTo(donate_now.value, { opacity: 0, y: 100 }, { opacity: 1, y: 0 });
});
</script>
