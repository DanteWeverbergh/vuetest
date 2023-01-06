<template>
  <div class="carousel">
    <div class="box" v-for="thumbnail in data.images" @click="selectThumbnail(thumbnail.id)">
      <img
        class="carousel__image"
        alt="active_image"
        :src="require(`../assets/images/${thumbnail.src}`)"
      />
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
  props: ["data"],
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
