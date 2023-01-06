<template>
  <div id="app">
    <p>{{ language }}</p>
    <p>{{ activeId }}</p>
    <LanguageSelector @update:lang="updateLang" />
    <ActiveThumbnail :data="data.data" :active="activeId" :lang="language" />
    <Carousel @update:thumbnail="updateActiveThumbnail" />
  </div>
</template>

<script lang="ts">
import LanguageSelector from "./components/LanguageSelector.vue";
import ActiveThumbnail from "./components/ActiveThumbnail.vue";
import Carousel from "./components/Carousel.vue";
import { defineComponent } from "vue";

import "./assets/styles/main.scss";

const data = require("./assets/data.json");

export default defineComponent({
  name: "app",
  data() {
    return {
      language: "en",
      activeId: 0,
      data: {
        type: Object,
        data,
      },
    };
  },
  components: {
    LanguageSelector,
    ActiveThumbnail,
    Carousel,
  },
  methods: {
    updateLang: function (lang: string) {
      this.language = lang;
    },
    updateActiveThumbnail: function (thumbnailId: Number) {
      alert(thumbnailId);
    },
  },
});
</script>
