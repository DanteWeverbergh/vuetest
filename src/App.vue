<template>
  <div id="app">
    <LanguageSelector @update:lang="updateLang" />
    <ActiveThumbnail :data="data.data[language]" :active="activeId" :lang="language" />
    <Carousel @update:thumbnail="updateActiveThumbnail" :data="data.data[language]" />
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
      language: "0",
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
      if (lang === "en") {
        this.language = "0";
      } else if (lang === "nl") {
        this.language = "1";
      }
    },
    updateActiveThumbnail: function (thumbnailId: number) {
      this.activeId = thumbnailId;
    },
  },
});
</script>
