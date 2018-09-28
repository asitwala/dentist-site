<template>
  <div class="ds-home-screen-1">
    <v-carousel dark hide-controls hide-delimiters>
      <v-carousel-item
        :src="require('@/static/img/dental-stock-photo-1.jpg')"
      ></v-carousel-item>
      <v-carousel-item
        :src="require('@/static/img/dental-stock-photo-2.jpg')"
      ></v-carousel-item>
    </v-carousel>
  </div>
</template>

<script>
export default {
  data() {
    return {
    };
  },
};

</script>

<style language="scss">
  .ds-home-screen-1 {
    width: 100%;
  }
</style>
