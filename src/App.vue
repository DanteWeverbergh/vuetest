<template>
  <div id="app">
    <LanguageSelector />
    <ActiveThumbnail :data="data.data" />
  </div>
</template>

<script lang="ts">
import LanguageSelector from "./components/LanguageSelector.vue";
import ActiveThumbnail from "./components/ActiveThumbnail.vue";

import "./assets/styles/main.scss";

const data = require("./assets/data.json");

export default {
  name: "app",
  data() {
    return {
      language: "en",
      active: 1,
      data: {
        type: Object,
        data,
      },
    };
  },
  components: {
    LanguageSelector,
    ActiveThumbnail,
  },
};
</script>
