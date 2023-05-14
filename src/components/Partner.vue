<template>
  <div class="partner-logo">
    <div class="container">
      <carousel
        class="logo-carousel"
        v-bind="settings"
        :breakpoints="breakpoints"
        :dots="false"
        :nav="false"
        :autoplay="false"
        :wrap-around="true"
      >
        <slide class="logo-item" v-for="partner in partners" :key="partner">
          <div class="tablecell-inner">
            <img :src="partner.image" alt="" />
          </div>
        </slide>
      </carousel>
    </div>
  </div>
</template>

<script>
import { ref } from "vue";
import "vue3-carousel/dist/carousel.css";
import { Carousel, Slide } from "vue3-carousel";
export default {
  // eslint-disable-next-line
  name: "Partner",
  components: {
    Carousel,
    Slide,
  },
  data: () => ({
    settings: {
      itemsToShow: 1,
      snapAlign: "center",
    },
    // breakpoints are mobile first
    // any settings not specified will fallback to the carousel settings
    breakpoints: {
      1200: {
        itemsToShow: 5,
        snapAlign: "center",
      },
    },
  }),
  setup() {
    const partners = ref([
      {
        image: "img/logo-carousel/logo-1.png",
      },
      {
        image: "img/logo-carousel/logo-2.png",
      },
      {
        image: "img/logo-carousel/logo-3.png",
      },
      {
        image: "img/logo-carousel/logo-4.png",
      },
      {
        image: "img/logo-carousel/logo-5.png",
      },
    ]);

    return {
      partners,
    };
  },
};
</script>

<style></style>
