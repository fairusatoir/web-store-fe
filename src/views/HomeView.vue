<template>
  <div class="home">
    <Header />
    <Hero />
    <ProductBanner />
  </div>
</template>

<script>
// @ is an alias to /src

import Header from "@/components/Header.vue";
import Hero from "@/components/Hero.vue";
import ProductBanner from "@/components/ProductBanner.vue";

export default {
  name: "HomeView",
  components: {
    Header,
    Hero,
    ProductBanner,
  },
};
</script>

<style scoped></style>
