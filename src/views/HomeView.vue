<template>
  <div class="home">
    <Header />
    <Hero />
    <ProductBanner />
    <Gallery />
    <Partner />
    <Footer />
  </div>
</template>

<script>
// @ is an alias to /src

import Header from "@/components/Header.vue";
import Hero from "@/components/Hero.vue";
import ProductBanner from "@/components/ProductBanner.vue";
import Gallery from "@/components/Gallery.vue";
import Partner from "@/components/Partner.vue";
import Footer from "@/components/Footer.vue";

export default {
  name: "HomeView",
  components: {
    Header,
    Hero,
    ProductBanner,
    Gallery,
    Partner,
    Footer,
  },
};
</script>

<style scoped></style>
