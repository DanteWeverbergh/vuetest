<template>
  <div>
    <select v-model="language" class="select" v-on:change="languageIsChanged">
      <option value="en">English</option>
      <option value="nl">Nederlands</option>
    </select>
  </div>
</template>

<script lang="ts">
import { defineComponent } from "vue";

export default defineComponent({
  data() {
    return {
      language: "en",
    };
  },
  methods: {
    languageIsChanged: function (lang: string): void {
      //
      this.$emit("update:lang", this.language);
    },
  },
});
</script>
