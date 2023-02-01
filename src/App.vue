<script setup>
  import { RouterView } from 'vue-router'
import SideBar from './views/SideBar.vue';
import Layout from './router/Layout.vue';
</script>

<template>
  <SideBar />
  <RouterView />
  <!-- <SideBar />
  <RouterView /> -->
</template>





<style>
  #app {
    min-height: 40rem;
    min-height: 40rem;
    display: flex;
  }

</style>