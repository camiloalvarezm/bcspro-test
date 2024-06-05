<script setup>
import Header from "./components/Header.vue";
import Dashboard from "./components/Dashboard.vue";
import Footer from "./components/Footer.vue";
</script>

<template>
  <div class="d-none d-lg-flex flex-column">
    <Header />
    <Dashboard />
    <Footer />
  </div>
  <div
    class="mobile-wrapper d-flex flex-column gap-3 d-lg-none vh-100 border align-items-center justify-content-center"
  >
    <img src="./assets/logo.svg" alt="logo" class="w-75" />
    <p class="text-center text-white mx-3">
      Para una experiencia completa, BCSPRO solo está disponible en escritorio.
    </p>
  </div>
</template>

<style scoped lang="scss">
@import "./style.scss";
.mobile-wrapper {
  background-color: $custom-bg-dark-color;
  border: none !important;

  img {
    animation: floatAnimation 3s infinite;
  }
}

@keyframes floatAnimation {
  0% {
    transform: translateY(0);
  }
  50% {
    transform: translateY(-10px);
  }
  100% {
    transform: translateY(0);
  }
}
</style>
