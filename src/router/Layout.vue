<script setup>
  import { RouterView } from 'vue-router'
  import SideBar from '../views/SideBar.vue';
</script>


<template>
  <div id="layout">
    <SideBar />
    <RouterView />
  </div>
  
</template>

<style scoped>
  #layout {
    min-height: 40rem;
    display: flex;
  }
</style>