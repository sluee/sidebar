<script setup>
    import MainNav from '@/Components/MainNav.vue'
    import { ref } from 'vue';

    let width = ref('w-[250px]')
    let hidden = ref("")

    function toggleWidth() {
        if(width.value == 'w-[250px]') {
            width.value = 'w-[50px]'
            hidden.value = "hidden"
        }else {
            width.value = ['w-[250px]']
            hidden.value = ""
        }
    }
</script>

<template>

<div class="flex min-h-screen">
    <div id="sidebar" class="bg-gray-100 p-6 duration-500" :class="width" style="position: relative;">
        <button class="text-xl text-tahiti" @click="toggleWidth" style="position: absolute; right: 10px; top:10px">
            <i class="fa-solid fa-bars"></i>
        </button>
        <div id="branding" :class="hidden">
            <img src="https://static.vecteezy.com/system/resources/previews/009/022/996/original/rqr-logo-rqr-letter-rqr-letter-logo-design-initials-rqr-logo-linked-with-circle-and-uppercase-monogram-logo-rqr-typography-for-technology-business-and-real-estate-brand-vector.jpg" alt="Logo"
                class="w-[170px] h-[170px] mx-auto rounded-full object-cover">
            <h1 class="text-3xl text-center text-tahiti my-6">RQR Internet services</h1>

        </div>
        <hr class="border-gray-600">

        <MainNav></MainNav>
    </div>
    <div id="container" class="flex-1 ">
        <slot />
    </div>
</div>

</template>
