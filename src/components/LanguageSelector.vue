<template>
  <div>
    <select v-model="language">
      <option value="en">English</option>
      <option value="nl">Nederlands</option>
    </select>
  </div>
</template>

<script lang="ts">
import { Component, Prop, Vue } from "vue-property-decorator";

@Component
export default class HelloWorld extends Vue {
  @Prop() private msg!: string;

  data() {
    return {
      language: "en",
    };
  }
}
</script>
