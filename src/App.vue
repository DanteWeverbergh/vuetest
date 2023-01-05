<template>
  <div id="app">
    <LanguageSelector />
    <thumbnails />
    <img alt="Vue logo" src="./assets/images/rotterdam.jpg" />
  </div>
</template>

<script lang="ts">
import { Component, Vue } from "vue-property-decorator";

import LanguageSelector from "./components/LanguageSelector.vue";
import Thumbnails from "./components/Thumbnails.vue";

@Component({
  components: {
    LanguageSelector,
    Thumbnails,
  },
})
export default class App extends Vue {}
</script>

<style lang="scss">
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
