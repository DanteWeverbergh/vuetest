<template>
  <div class="activeThumbnail">
    <p class="activeThumbnail__description">
      {{ data.images[active].description }}
    </p>

    <img
      class="activeThumbnail__image"
      alt="active_image"
      :src="require(`../assets/images/${data.images[active].src}`)"
    />
  </div>
</template>

<script lang="ts">
import { defineComponent } from "vue";

export default defineComponent({
  name: "ActiveThumbnail",
  props: ["data", "active", "lang"],
  data() {
    return {
      //
      id: 0,
      language: "en",
    };
  },
});
</script>
