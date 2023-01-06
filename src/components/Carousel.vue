<template>
  <h1>hkmhh</h1>
</template>

<script lang="ts">
import { Component, Prop, Vue } from "vue-property-decorator";
import "vue3-carousel/dist/carousel.css";
import { Carousel, Slide, Pagination, Navigation } from "vue3-carousel";

@Component
export default class CarouselComponent extends Vue {
  data() {
    return {
      active: "1",
    };
  }
}
</script>
