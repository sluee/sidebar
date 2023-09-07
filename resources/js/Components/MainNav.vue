<script setup>
import { Link } from '@inertiajs/vue3';
import { defineProps } from 'vue';

    defineProps({
        opensidebar: Boolean,
    })
</script>

<template>
<div class="main-nav" :class="opensidebar ? 'hidden' : ''">
    <Link href="#">
        <i class="fa fa-home"></i> <span v-show="!opensidebar">Home</span>
    </Link>
    <Link href="#">
        <i class="fa fa-question"></i> <span v-show="!opensidebar">About Us</span>
    </Link>
    <Link href="#">
        <i class="fa-solid fa-cart-shopping"></i> <span v-show="!opensidebar">Products</span>
    </Link>
    <Link href="#">
        <i class="fa-regular fa-images"></i> <span v-show="!opensidebar">Gallery</span>
    </Link>
    <Link href="#">
        <i class="fa-solid fa-phone-volume"></i> <span v-show="!opensidebar">Contact Us</span>
    </Link>
</div>
</template>


