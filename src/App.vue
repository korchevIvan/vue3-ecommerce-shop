<template>
  <div class="container">
    <Header/>
    <router-view/>
    <Footer/>
  </div>
</template>

<script setup>
import Header from '@/components/Layuot/Header.vue'
import Footer from '@/components/Layuot/Footer.vue'
</script>

<style lang="scss">
@import "assets/styles/global";
</style>