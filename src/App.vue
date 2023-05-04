<script setup>
import { RouterLink, RouterView } from "vue-router";
import Header from "./components/Header/index.vue";
import Footer from "./components/Footer/index.vue";
</script>

<template>
  <div class="common-layout">
    <Header />
    <Footer />
  </div>
</template>
<style>
.common-layout {
  position: relative;
  height: 100%;
  min-height: 100vh;
}
</style>
