<template>
  <div class="carousel">
    <div class="box" @click="selectThumbnail(0)">
      <img class="carousel__image" alt="active_image" src="../assets/images/rotterdam.jpg" />
    </div>
    <div class="box" @click="selectThumbnail(1)">
      <img class="carousel__image" alt="active_image" src="../assets/images/valletta.jpg" />
    </div>
    <div class="box" @click="selectThumbnail(2)">
      <img class="carousel__image" alt="active_image" src="../assets/images/vallettaPasen.jpg" />
    </div>
    <div class="box" @click="selectThumbnail(3)">
      <img class="carousel__image" alt="active_image" src="../assets/images/blueLagoon.jpg" />
    </div>
    <div class="box" @click="selectThumbnail(4)">
      <img class="carousel__image" alt="active_image" src="../assets/images/deNacht.jpg" />
    </div>
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
