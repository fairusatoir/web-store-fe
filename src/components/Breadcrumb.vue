<template>
  <!-- Breadcrumb Section Begin -->
  <div class="breacrumb-section">
    <div class="container">
      <div class="row">
        <div class="col-lg-12">
          <div class="breadcrumb-text product-more text-left">
            <router-link to="/"><i class="fa fa-home"></i> Home</router-link>
            <span>{{ routeNow }}</span>
          </div>
        </div>
      </div>
    </div>
  </div>
  <!-- Breadcrumb Section End -->
</template>

<script>
export default {
  // eslint-disable-next-line
  name: "Breadcrumb",
  props: ["routeNow"],
};
</script>

<style></style>
