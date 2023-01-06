<template>
  <div>
    <select class="select" v-on:change="languageIsChanged">
      <option value="en">English</option>
      <option value="nl">Nederlands</option>
    </select>
  </div>
</template>

<script lang="ts">
export default {
  props: ["language"],
  data() {
    return {};
  },
  methods: {
    languageIsChanged: function (): void {
      //
    },
  },
};
</script>
