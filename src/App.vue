<template>
  <div id="app">
    <p>{{ language }}</p>
    <LanguageSelector @update:test="updateTest" />
    <ActiveThumbnail :data="data.data" :active="activeId" />
    <Carousel />
  </div>
</template>

<script lang="ts">
import LanguageSelector from "./components/LanguageSelector.vue";
import ActiveThumbnail from "./components/ActiveThumbnail.vue";
import Carousel from "./components/Carousel.vue";

import "./assets/styles/main.scss";

const data = require("./assets/data.json");

export default {
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
    updateTest: function (value: string) {
      alert("udpate app");
    },
  },
};
</script>
