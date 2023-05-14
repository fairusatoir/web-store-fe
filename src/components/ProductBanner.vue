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
            :autoplay="4000"
            :wrap-around="true"
          >
            <slide
              class="product-item"
              v-for="imgProduct in products"
              :key="imgProduct"
            >
              <div class="product-wrapper">
                <div class="pi-pic">
                  <img :src="imgProduct" alt="" />
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
            <template #addons>
              <div class="mt-4">
                <Pagination />
              </div>
            </template>
          </carousel>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
import "vue3-carousel/dist/carousel.css";
import { Carousel, Slide, Pagination } from "vue3-carousel";
export default {
  name: "ProductBanner",
  components: {
    Carousel,
    Slide,
    Pagination,
  },
  data() {
    return {
      products: [
        "img/products/women-1.jpg",
        "img/products/women-2.jpg",
        "img/products/women-3.jpg",
        "img/products/women-4.jpg",
      ],
      settings: {
        itemsToShow: 1,
        snapAlign: "center",
      },
      // breakpoints are mobile first
      // any settings not specified will fallback to the carousel settings
      breakpoints: {
        768: {
          itemsToShow: 2,
          snapAlign: "start",
        },
        1440: {
          itemsToShow: 3,
          snapAlign: "start",
        },
      },
    };
  },
};
</script>

<style scoped>
@media only screen and (min-width: 1024px) {
  .product-wrapper .pi-pic img {
    height: 650px;
  }
}
</style>
