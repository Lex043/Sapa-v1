<template>
    <section class="bg-[#222222] border-b-[1px] border-[#BABABA]">
        <section
            class="flex justify-between items-center px-4 py-3 md:py-4 lg:w-[80%] lg:mx-auto"
        >
            <section class="flex gap-16 items-center">
                <div class="flex items-center gap-1">
                    <img src="../assets/logo.svg" alt="" />
                    <span class="text-[1.75rem] font-semibold text-white text"
                        >Sapa</span
                    >
                </div>

                <div>
                    <nav
                        class="hidden text-white text-base md:flex md:items-center md:gap-8"
                    >
                        <a href="#">About us</a>
                        <a href="#">Sapa</a>
                        <a href="#">Help</a>
                        <a href="#">Contacts us</a>
                    </nav>
                </div>
            </section>

            <div>
                <button @click="toggleMenu" class="text-3xl text-white cursor-pointer md:hidden">&#9776</button>
                <button
                    class="hidden bg-[#215056] py-2 px-2 w-fit rounded-md md:flex gap-1 items-center text-white"
                >
                    Urgent tukay
                    <span
                        ><img
                            src="../assets/pleading-face.svg"
                            alt="pleading face"
                    /></span>
                </button>
            </div>
        </section>

        <section
            
            @click="toggleMenu"
            :class="{ visible: isMenuVisible }"
            class="text-base absolute top-4 hidden w-full origin-top animate-open-menu flex-col bg-[#222222] z-50"
        >
            <button class="self-end px-4 text-4xl text-white">&times;</button>
            <nav class="flex min-h-screen text-white flex-col pl-4 md:block">
                <a href="#" class="w-full py-2 text-start"> About us </a>
                <a href="#" class="w-full py-2 text-start"> Sapa </a>
                <a href="#" class="w-full py-2 text-start"> Help </a>
                <a href="#" class="w-full py-2 text-start">Contacts us</a>

                <button
                    class="bg-[#215056] py-2 px-2 w-fit rounded-md flex gap-1 items-center text-white"
                >
                    Urgent tukay
                    <span
                        ><img
                            src="../assets/pleading-face.svg"
                            alt="pleading face"
                    /></span>
                </button>
            </nav>
        </section>
    </section>
</template>

<script setup>
import { ref } from "vue";
const isMenuVisible = ref(false);

const toggleMenu = () => {
  isMenuVisible.value = !isMenuVisible.value;
};

</script>

<style lang="css" scoped>
.visible {
    display: flex !important;
}
</style>
