<template>
  <div class="carousel">
    <div class="box1" @click="selectThumbnail(0)">0</div>
    <div class="box2" @click="selectThumbnail(1)">1</div>
  </div>
</template>

<script lang="ts">
//import { Carousel, Slide } from "vue-carousel";
import { defineComponent } from "vue";
import Vue from "vue";

import { Carousel, Slide } from "vue-snap";
import "vue-snap/dist/vue-snap.css";

export default defineComponent({
  name: "Carousel",
  data() {
    return {};
  },
  components: { Carousel, Slide },
  methods: {
    selectThumbnail: function (thumbnailId: number): void {
      this.$emit("update:thumbnail", thumbnailId);
    },
    test: function () {
      alert("click");
    },
  },
});
</script>
