<template>
  <div class="home">
    <Header />
    <Hero />
    <ProductBanner />
    <Gallery />
  </div>
</template>

<script>
// @ is an alias to /src

import Header from "@/components/Header.vue";
import Hero from "@/components/Hero.vue";
import ProductBanner from "@/components/ProductBanner.vue";
import Gallery from "@/components/Gallery.vue";

export default {
  name: "HomeView",
  components: {
    Header,
    Hero,
    ProductBanner,
    Gallery,
  },
};
</script>

<style scoped></style>
