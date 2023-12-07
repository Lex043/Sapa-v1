<template>
    <section class="bg-[#222222]">
        <section
            class="px-4 pt-5 lg:w-[80%] lg:mx-auto lg:flex lg:items-center lg:justify-between"
        >
            <div class="flex flex-col gap-4 lg:max-w-[28rem]">
                <header class="flex flex-col gap-4 text-white overflow-hidden">
                    <h1 class="font-bold text-[3.25rem]" ref="hero_title">
                        Na beg , we dey beg
                    </h1>
                    <p class="text-[1rem] font-normal" ref="hero_subtitle">
                        Urgent 2k is a valid Nigerian currency. It is more than
                        an emergency fund; it is a lifesaver, a life jacket when
                        you are drowning. In fact, this currency has officially
                        been recognized.
                    </p>
                    <button
                        class="bg-[#215056] py-2 px-2 w-fit rounded-md flex gap-1 items-center"
                        ref="hero_btn"
                    >
                        Urgent tukay
                        <span
                            ><img
                                src="../assets/pleading-face.svg"
                                alt="pleading face"
                        /></span>
                    </button>
                </header>

                <div>
                    <p class="text-white text-[0.85rem]" ref="support">
                        Who suppports us
                    </p>

                    <figure
                        class="flex flex-wrap gap-2 pt-4 text-white overflow-hidden"
                    >
                        <img
                            class="w-[6rem]"
                            ref="paypal"
                            src="../assets/paypal.svg"
                            alt="paypal"
                        />
                        <img
                            class="w-[6rem]"
                            ref="opay"
                            src="../assets/opay.svg"
                            alt="opay"
                        />
                        <img
                            ref="palmpay"
                            class="w-[6rem] object-contain"
                            src="../assets/palmpay.svg"
                            alt="palmpay"
                        />
                        <img
                            ref="kuda"
                            class="w-[6rem] object-contain"
                            src="../assets/kuda.svg"
                            alt="kuda"
                        />
                    </figure>
                </div>
            </div>

            <figure>
                <img src="../assets/heroImg.svg" alt="hero image" />
            </figure>
        </section>
    </section>
</template>

<script setup>
import gsap from "gsap";
import { onMounted, ref } from "vue";

const hero_title = ref(null);
const hero_subtitle = ref(null);
const hero_btn = ref(null);
const support = ref(null);
const paypal = ref(null);
const opay = ref(null);
const palmpay = ref(null);
const kuda = ref(null);

onMounted(() => {
    const timeline = gsap.timeline({
        defaults: { duration: 0.75, ease: "Power3.easeOut" },
    });

    timeline.fromTo(
        hero_title.value,
        { opacity: 0, y: 100 },
        { opacity: 1, y: 0, duration: 0.6, delay: 1 }
    );

    timeline.fromTo(
        hero_subtitle.value,
        { opacity: 0, y: 100 },
        { opacity: 1, y: 0 },
        "<50%"
    );

    timeline.fromTo(
        hero_btn.value,
        { opacity: 0, y: 100 },
        { opacity: 1, y: 0 },
        "<60%"
    );

    timeline.fromTo(
        support.value,
        { opacity: 0, y: 50 },
        { opacity: 1, y: 0 },
        "<40%"
    );

    //
    timeline.fromTo(
        paypal.value,
        { opacity: 0, y: 50 },
        { opacity: 1, y: 0 },
        "<30%"
    );

    timeline.fromTo(
        opay.value,
        { opacity: 0, x: 50 },
        { opacity: 1, x: 0 },
        "<30%"
    );

    timeline.fromTo(
        palmpay.value,
        { opacity: 0, y: -50 },
        { opacity: 1, y: 0 },
        "<30%"
    );

    timeline.fromTo(
        kuda.value,
        { opacity: 0, y: 50 },
        { opacity: 1, y: 0 },
        "<30%"
    );
});
</script>
