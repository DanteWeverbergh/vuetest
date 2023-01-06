<template>
  <div>
    <select v-model="language" class="select">
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
};
</script>
