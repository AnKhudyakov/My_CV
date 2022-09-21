<script setup>
import { RouterView } from 'vue-router';
import SiteHeader from './components/SiteHeader.vue';
import MobileHeader from './components/MobileHeader.vue';
</script>

<template>
  <header>
    <SiteHeader></SiteHeader>
    <MobileHeader></MobileHeader>
  </header>

  <main class="page">
    <Transition name="slide-page">
      <RouterView />
    </Transition>
  </main>
</template>

<style scoped>
header {
  display: block;
}
.page {
  padding-left: 160px;
  width: 100%;
  height: 100%;
  margin: 0;
}
.slide-page-enter-active {
  transition: all 0.7s ease-out;
}

.slide-page-leave-active {
  transition: all 0.7s ease-in;
}

.slide-page-enter-from,
.slide-page-leave-to {
  transform: translateX(500px);
  opacity: 0;
}

@media only screen and (max-width: 991px) {
  .page {
    padding-top: 50px;
    padding-left: 0;
  }
}
</style>
