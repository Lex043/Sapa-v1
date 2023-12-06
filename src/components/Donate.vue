<template>
    <section class="bg-[#FAFBFC] py-10">
        <div class="flex flex-col gap-3 px-2 lg:w-[80%] lg:mx-auto">
            <div class="flex flex-col gap-4">
                <h1
                    class="text-[#272D37] text-[2rem] text-center font-semibold lg:max-w-[50rem] lg:mx-auto"
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
                        class="bg-[#215056] text-white text-sm py-2 px-2 w-fit md:w-[8rem] rounded-md flex gap-1 items-center justify-center"
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

<script setup></script>
