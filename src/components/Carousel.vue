<template>
  <div class="carousel">
    <p>{{ active }}</p>
    <div class="box1" @click="selectThumbnail(0)">0</div>
    <div class="box2" @click="selectThumbnail(1)">1</div>
  </div>
</template>

<script lang="ts">
//import { Carousel, Slide } from "vue-carousel";
import { defineComponent } from "vue";

export default defineComponent({
  name: "Carousel",
  data() {
    return {
      active: 0,
    };
  },
  components: {},
  methods: {
    selectThumbnail: function (thumbnailId: number): void {
      this.active = thumbnailId;
    },
  },
});
</script>
