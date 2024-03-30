<script setup>
import hero from "./components/hero.vue";
import animatePositionX from "./components/animatePositionX.vue";
import animatePositionY from "./components/animatePositionY.vue";
import animateTextRemove from "./components/animateTextRemove.vue";
import animateText from "./components/animateText.vue";
import animateBgChangeColor from "./components/animateBgChangeColor.vue";
import animateChangeColor from "./components/animateChangeColor.vue";
import animateOpacityChange from "./components/animateOpacityChange.vue";
import animateScale from "./components/animateScale.vue";
import animateRotate from "./components/animateRotate.vue";
import animateSVGStroke from "./components/animateSVGStroke.vue";
import animateSVGStrokeStagger from "./components/animateSVGStrokeStagger.vue";
import animatePin from "./components/animatePin.vue";
</script>

<template>
  <div class="background">
    <hero />
    <animatePositionX />
    <animatePositionY />
    <animateTextRemove />
    <animateText />
    <animateBgChangeColor />
    <animateChangeColor />
    <animateOpacityChange />
    <animateScale />
    <animateRotate />
    <animateSVGStroke/>
    <animateSVGStrokeStagger />
    <animatePin />
  </div>
</template>

<style scoped>
.background {
  background-color: #e7e7e7;
  z-index: -1;
}
</style>
