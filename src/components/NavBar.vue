<script setup>
import { ref } from 'vue';

const active = ref(false);

let toggleSearch = () => {
  active.value = !active.value;
};
</script>

<template>
    <nav class="mt-3 mx-4 flex justify-between">
        <div class="flex gap-x-4 ">
            <button  class="hover:bg-gray-200 rounded hidden md:block">
                <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" class="w-6 h-6">
                    <path stroke-linecap="round" stroke-linejoin="round" d="M3.75 6.75h16.5M3.75 12h16.5m-16.5 5.25h16.5" />
                </svg>
            </button>
            <div class="flex gap-x-2">
                <img class="w-9 h-9" src="../assets/icons/youtube.png" alt="" srcset="">
                <h1 class="font-semibold text-2xl">Youtube <sup class="text-sm">CL</sup></h1>
            </div>
        </div>
        <input class="border-1 w-2/4 px-5"type="search" v-show="active" placeholder="Ingrese su búsqueda" @keydown.enter="search">    

        <div class="flex align-middle gap-x-8">
            <button class="" @click="toggleSearch">
                <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" class="w-6 h-6">
                    <path stroke-linecap="round" stroke-linejoin="round" d="m21 21-5.197-5.197m0 0A7.5 7.5 0 1 0 5.196 5.196a7.5 7.5 0 0 0 10.607 10.607Z" />
                </svg>
            </button>
            <button class="rounded-full w-9 h-9 bg-emerald-600">
                <span>V</span>
            </button>
        </div>
    </nav>
</template>
