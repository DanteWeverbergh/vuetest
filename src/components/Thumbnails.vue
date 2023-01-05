<template>
  <div>
    <h1>Thumbnails</h1>
  </div>
</template>

<script lang="ts">
import { Component, Prop, Vue } from "vue-property-decorator";

@Component
export default class HelloWorld extends Vue {
  @Prop() private msg!: string;

  data() {
    return {
      active: "1",
    };
  }
}
</script>
