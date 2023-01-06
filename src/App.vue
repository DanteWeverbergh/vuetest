<template>
  <div id="app">
    {{ language }}
    <LanguageSelector :language="language" />
    <ActiveThumbnail :data="data.data" :active="activeId" />
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
  },
};
</script>
