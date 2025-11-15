<template>
    <header class="">
        <nav class="md:flex hidden bg-white p-4 items-center justify-between">

        <div class="">
            <ul class=" flex gap-4 justify-center items-center">
                <h1>logo</h1>
            </ul>
            
        </div>
        <div class="">
            <ul class=" flex gap-4 justify-center items-center">
                <li>projects</li>
                <li>contact</li>
                <li>about</li>
                <li>music</li>
            </ul>
            
        </div>
        <div class="">
            <ul class=" flex gap-4 justify-center items-center">
                <i class="pi pi-linkedin"></i>
                <i class="pi pi-facebook"></i>
                <i class="pi pi-instagram"></i>
                <i class="pi pi-github"></i>
                <i class="pi pi-youtube"></i>
                <i class="pi pi-soundcloud"></i>
            </ul>
            
        </div>
        </nav>

    </header>
    <header class="md:hidden">
                    <div class="">
            <Burger/>
        </div>
    </header>

</template>
<script setup>

import Burger from './Burger.vue';
import 'primeicons/primeicons.css'
</script>
