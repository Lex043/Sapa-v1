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

                        <Link to="/register" className="ml-10">
                            <Button>Register</Button>
                        </Link>
                    </nav>
                </div>
            </section>

            <div>
                <button id="hamburger-button" class="text-3xl text-white cursor-pointer md:hidden">&#9776</button>
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
            id="mobile-menu"
            class="text-x absolute top-0 hidden w-full origin-top animate-open-menu flex-col bg-[#150e28] z-50"
        >
            <button class="self-end px-4 text-4xl">&times;</button>
            <nav class="flex min-h-screen flex-col pl-4 md:block">
                <a href="#" class="w-full py-2 text-start"> About us </a>
                <a href="#" class="w-full py-2 text-start"> Sapa </a>
                <a href="#" class="w-full py-2 text-start"> Help </a>

                <div to="/contact" class="w-full py-2 text-start">Contact</div>

                <div
                    to="/register"
                    className="w-28 rounded-sm mt-2  bg-gradient-to-r from-[#FF26B9] via-[#d434fe] to-[#903aff] py-2 text-white text-center"
                >
                    Register
                </div>
            </nav>
        </section>
    </section>
</template>

<script setup></script>
