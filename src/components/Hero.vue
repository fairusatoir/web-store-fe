<template>
  <!-- Hero Section Begin -->
  <section class="hero-section">
    <carousel
      class="hero-items"
      :items="1"
      :nav="false"
      :autoplay="5000"
      :wrap-around="true"
    >
      <slide v-for="slide in slides" :key="slide">
        <div
          class="single-hero-items set-bg"
          :style="{ backgroundImage: `url('${slide.image}')` }"
        >
          <div class="container">
            <div class="row content-text-items">
              <div class="col-lg-5 text-left">
                <span>Bag,kids</span>
                <h1>Black friday</h1>
                <p>
                  Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed
                  do eiusmod tempor incididunt ut labore et dolore
                </p>
                <a class="primary-btn" href="#">Shop Now</a>
              </div>
            </div>
          </div>
        </div>
      </slide>
      <template #addons>
        <navigation />
        <pagination />
      </template>
    </carousel>
  </section>
  <!-- Hero Section End -->
</template>

<script>
import { ref } from "vue";
import "vue3-carousel/dist/carousel.css";
import { Carousel, Slide, Pagination, Navigation } from "vue3-carousel";
export default {
  // eslint-disable-next-line
  name: "Hero",
  components: {
    Carousel,
    Slide,
    Pagination,
    Navigation,
  },
  setup() {
    const slides = ref([
      {
        image: "/img/hero-1.jpg",
      },
      {
        image: "/img/hero-2.jpg",
      },
      {
        image: "/img/hero-1.jpg",
      },
      {
        image: "/img/hero-2.jpg",
      },
      {
        image: "/img/hero-1.jpg",
      },
      {
        image: "/img/hero-2.jpg",
      },
      {
        image: "/img/hero-1.jpg",
      },
      {
        image: "/img/hero-2.jpg",
      },
    ]);

    return {
      slides,
    };
  },
};
</script>

<style scoped>
.content-text-items span,
.content-text-items h1,
.content-text-items p,
.content-text-items .primary-btn {
  opacity: 1;
  top: -75px;
}

.set-bg {
  width: 100%;
  height: 550px;
}

@media (max-width: 768px) {
  .content-text-items span,
  .content-text-items h1,
  .content-text-items p,
  .content-text-items .primary-btn {
    opacity: 1;
    top: 25px;
  }
}

@media (max-width: 480px) {
  .content-text-items span,
  .content-text-items h1,
  .content-text-items p,
  .content-text-items .primary-btn {
    opacity: 1;
    top: -25px;
  }
}
</style>
