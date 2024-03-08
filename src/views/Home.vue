<script setup>

import Caroulsel from '../components/Caroulsel.vue';
import FooterNav from '../components/FooterNav.vue';
import HeroSection from '../components/HeroSection.vue';
import SideBar from '../components/SideBar.vue';

</script>
<template lang="html">
    <main class="flex">
        <SideBar class="hidden lg:block"/>
        <div class="mt-5">
            <Caroulsel/>
            <HeroSection class="mt-5"/>
            <FooterNav />
        </div>
    </main>
</template>
