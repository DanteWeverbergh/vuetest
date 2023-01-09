<template>
  <div class="carousel">
    <carousel-3d
      :space="365"
      :clickable="false"
      :controls-visible="true"
      :width="250"
      :height="250"
      :display="5"
    >
      <slide v-for="(thumbnail, i) in data.images" :index="i">
        <div @click="selectThumbnail(thumbnail.id)" class="carousel__card">
          <img
            @click="alert('hkhhlk')"
            alt="active_image"
            :src="require(`../assets/images/${thumbnail.src}`)"
          />
        </div>
      </slide>
    </carousel-3d>

    <!--
    <div class="box" v-for="thumbnail in data.images" @click="selectThumbnail(thumbnail.id)">
      <img
        class="carousel__image"
        alt="active_image"
        :src="require(`../assets/images/${thumbnail.src}`)"
      />
    </div>
    -->
  </div>
</template>

<script lang="ts">
//import { Carousel, Slide } from "vue-carousel";
import { defineComponent } from "vue";
import Vue from "vue";

import { Carousel3d, Slide } from "vue-carousel-3d";

export default defineComponent({
  name: "Carousel",
  data() {
    return {};
  },
  props: ["data"],
  components: { Carousel3d, Slide },
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
