<template>
  <div class="activeThumbnail">
    <p class="activeThumbnail__description">{{ data.en.images[active].description }}</p>

    <img class="activeThumbnail__image" alt="active_image" src="../assets/images/rotterdam.jpg" />
  </div>
</template>

<script lang="ts">
export default {
  name: "ActiveThumbnail",
  props: ["data", "active"],
  data() {
    return {
      //
      id: 0,
      language: "en",
    };
  },
};
</script>
