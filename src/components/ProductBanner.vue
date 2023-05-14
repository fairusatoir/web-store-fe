<template>
  <section class="women-banner spad">
    <div class="container-fluid">
      <div class="row">
        <div class="col-lg-12 mt-5">
          <carousel
            class="product-slider"
            v-bind="settings"
            :breakpoints="breakpoints"
            :dots="false"
            :nav="false"
            :autoplay="false"
            :wrap-around="true"
          >
            <slide
              class="product-item"
              v-for="itemProduct in products"
              :key="itemProduct"
            >
              <div class="product-wrapper">
                <div class="pi-pic">
                  <img :src="itemProduct.image" height="750" alt="" />
                  <ul>
                    <li class="w-icon active">
                      <a href="#"><i class="icon_bag_alt"></i></a>
                    </li>
                    <li class="quick-view"><a href="#">+ Quick View</a></li>
                  </ul>
                </div>
                <div class="pi-text">
                  <div class="catagory-name">Shoes</div>
                  <a href="#">
                    <h5>Guangzhou sweater</h5>
                  </a>
                  <div class="product-price">$13.00</div>
                </div>
              </div>
            </slide>
          </carousel>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
import { ref } from "vue";
import "vue3-carousel/dist/carousel.css";
import { Carousel, Slide } from "vue3-carousel";
export default {
  name: "ProductBanner",
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
        itemsToShow: 3,
        snapAlign: "center",
      },
    },
  }),
  setup() {
    const products = ref([
      {
        image: "img/products/women-1.jpg",
      },
      {
        image: "img/products/women-2.jpg",
      },
      {
        image: "img/products/women-3.jpg",
      },
      {
        image: "img/products/women-1.jpg",
      },
      {
        image: "img/products/women-2.jpg",
      },
      {
        image: "img/products/women-3.jpg",
      },
    ]);

    return {
      products,
    };
  },
};
</script>

<style scoped>
.pi-pic {
  height: 500px;
}
.pi-pic img {
  max-height: 100%;
  width: auto;
}

@media only screen and (min-width: 1201px) {
  .product-item {
    margin-right: 5px;
  }
}
</style>
