<script setup>
import { ref } from 'vue';
import data from '../data/videos.json';

const thumbnail = ref(data);
</script>

<template lang="">
  <section class="flex-col w-full md:grid md:grid-cols-2 lg:grid-cols-3 md:gap-x-5 auto-cols-max">
    <div v-for="item in thumbnail" :key="item.id" class="md:rounded-md">
      <img class="w-full h-72 md:rounded-md" :src=item.imagen alt="" srcset="">
      <div class="flex  items-center mb-5">
        <img class="w-16 h-16" :src=item.profilePhoto alt="" srcset="">
        <div class="flex flex-col">
          <p class="text-xl">{{ item.titulo }}</p>
          <div class="flex gap-x-1 text-gray-500 text-xs">
            <span>{{ item.chanelName }}</span>
            <span>&#8226;</span>
            <span>{{ item.visitCount }}</span>
            <span>&#8226;</span>
            <span>{{ item.referenceDate }}</span>
          </div>
        </div>
        <button class="relative flex items-end ml-auto">
          <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" class="w-6 h-6">
              <path stroke-linecap="round" stroke-linejoin="round" d="M12 6.75a.75.75 0 1 1 0-1.5.75.75 0 0 1 0 1.5ZM12 12.75a.75.75 0 1 1 0-1.5.75.75 0 0 1 0 1.5ZM12 18.75a.75.75 0 1 1 0-1.5.75.75 0 0 1 0 1.5Z" />
            </svg>
        </button>
      </div>
    </div>
  </section>
</template>
