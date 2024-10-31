<script setup>
import { RouterView } from "vue-router";
import Navbar from "./components/Navbar.vue";
import Footer from "./components/Footer.vue";
</script>

<template>
  <div class="max-w-6xl mx-auto">
    <Navbar />
    <div class="border my-3 p-4">
      <RouterView />
    </div>
    <Footer />
  </div>
</template>
