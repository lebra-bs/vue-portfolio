<template>
    <header>
        <div class="flex justify-between items-center p-8 lg:px-12 relative z-20">
            <div class="text-3xl font-bold">LOGO</div>

            <div class="md:hidden z-30" @click="isMenuOpen = !isMenuOpen">
                <button class="block focus:outline-none">
                <span v-if="isMenuOpen" class="text-5xl md:text-primary">
                    <Icon icon="material-symbols:close"/>
                </span>
                <span v-else class="text-5xl md:text-primary">
                    <Icon icon="material-symbols:menu"/>
                </span>
                </button>
            </div>

            <nav :class="[
                `fixed inset-0 z-20 flex flex-col items-center justify-center md:relative md:flex md:justify-between md:flex-row ${isMenuOpen ? 'block':'hidden'}`
            ]"
            >
            <ul class="flex flex-col items-center space-y-5 md:flex-row md:space-x-5 md:space-y-0">
                <li v-for="item in Menu" :key="item.name">
                    <a href="item.href" class="block transition ease-linear md:text-lg lg:text-xl font-bold" @click="scrollToSection(item.href)">
                        {{ item.name }}
                    </a>
                </li>
            </ul>
            </nav>

        </div>
    </header>
</template>
<script setup>
import { ref } from 'vue';
const isMenuOpen = ref (false);
const Menu = ref ([
    {name:'Projects', href:'#projects'},
    {name:'Skills', href:'#skills'},
    {name:'Contact', href:'#contact'},
    {name:'About', href:'#about'},
]);

const scrollToSection = (href) =>{
    isMenuOpen.value = false;
    const section = document.querySelector(href);
    if(section){
        section.scrollIntoView({behavior:'smooth'});
    }
}
</script>
