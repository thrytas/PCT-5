<template>
  <StackLayout verticalAlignment="bottom" class="bottom-container">
    <GridLayout class="red-bottom"></GridLayout>
    <GridLayout class="blue-bottom"></GridLayout>
  </StackLayout>
</template>

<script lang="ts">
import Vue from "nativescript-vue";
import { Component, Prop } from "vue-property-decorator";

@Component
export default class ActionBarBottom extends Vue {
  msg: string = "ActionBarBottom";

  openLink() {
    console.log("HI");
    //openUrl("www.google.com");
  }
}
</script>

<style scoped lang="scss">
@import "@nativescript/theme/scss/variables/blue";

// Custom styles
.fas {
  @include colorize($color: accent);
}

.blue-top {
  background-image: linear-gradient(to right, #2c3153, #555fa4);
  height: 50%;
}

.red-top {
  background-color: #a04f5f;
  clip-path: polygon(0 0, 0 60%, 100% 0);
  height: 25%;
}

.blue-bottom {
  background-image: linear-gradient(to right, #2c3153, #555fa4);
  height: 50%;
}

.red-bottom {
  background-color: #a04f5f;
  clip-path: polygon(0 100%, 100% 100%, 100% 40%);
  height: 50%;
}
</style>
