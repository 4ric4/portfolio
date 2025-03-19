
<template>
  <div class="bg-[#111827] min-h-screen">
    <NavBar />
  </div>

</template>


<script setup>
import { defineAsyncComponent } from 'vue'

const NavBar = defineAsyncComponent(() => import('@/components/NavBar.vue'))
</script>