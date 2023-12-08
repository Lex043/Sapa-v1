<template>
    <section class="bg-[#FFFFFF] py-12" ref="currency_container">
        <div class="lg:w-[80%] lg:mx-auto px-2 flex flex-col gap-2 lg:gap-12">
            <header class="text-center flex flex-col gap-4 overflow-hidden">
                <h1
                    class="text-[#272D37] font-bold text-[2rem]"
                    ref="currency_title"
                >
                    Our Currencies
                </h1>
                <p class="text-[#5F6D7E] text-[1rem]" ref="currency_subtitle">
                    These currencies has been saving lives since 1900
                </p>
            </header>
            <section class="flex flex-col md:flex-row gap-6">
                <div class="flex flex-col gap-2">
                    <img src="../assets/Rectangle 1.png" alt="" />

                    <h1 class="text-[#272D37] font-semibold">
                        We accepts all forms of digital help
                    </h1>
                    <p class="text-[#5F6D7E] text-base">
                        Urgent 2k is a valid Nigerian currency. It is more than
                        an emergency fund; it is a lifesaver, a life jacket when
                        you are drowning. In fact, this currency has officially
                        been recognized.
                    </p>

                    <div class="flex justify-between">
                        <p class="text-[#272D37] text-sm">Created</p>
                        <p class="text-[#5F6D7E] text-sm">3rd Dec</p>
                    </div>
                </div>
                <div class="flex flex-col gap-2">
                    <img src="../assets/Rectangle 2.png" alt="" />

                    <h1 class="text-[#272D37] font-semibold">
                        We accepts all forms of digital help
                    </h1>
                    <p class="text-[#5F6D7E] text-base">
                        Urgent 2k is a valid Nigerian currency. It is more than
                        an emergency fund; it is a lifesaver, a life jacket when
                        you are drowning. In fact, this currency has officially
                        been recognized.
                    </p>

                    <div class="flex justify-between">
                        <p class="text-[#272D37] text-sm">Created</p>
                        <p class="text-[#5F6D7E] text-sm">3rd Dec</p>
                    </div>
                </div>
            </section>
        </div>
    </section>
</template>

<script setup>
import gsap from "gsap";
import { ScrollTrigger } from "gsap/ScrollTrigger";
import { onMounted, ref } from "vue";
gsap.registerPlugin(ScrollTrigger);

const currency_container = ref(null);
const currency_title = ref(null);
const currency_subtitle = ref(null);

onMounted(() => {
    const tl = gsap.timeline({
        scrollTrigger: {
            trigger: currency_container.value,
            start: "top center",
            once: true,
        },
    });

    tl.fromTo(
        currency_title.value,
        { opacity: 0, y: 100 },
        { opacity: 1, y: 0 }
    );

    tl.fromTo(
        currency_subtitle.value,
        { opacity: 0, y: 100 },
        { opacity: 1, y: 0 }
    );
});
</script>
