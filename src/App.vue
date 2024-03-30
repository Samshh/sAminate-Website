<script setup>
import hero from "./components/hero.vue";
import animatePositionXY from "./components/animatePositionXY.vue";
import animateText from "./components/animateText.vue";
import animateChangeColor from "./components/animateChangeColor.vue";
import animateScale from "./components/animateScale.vue";
import animateRotate from "./components/animateRotate.vue";
import animateSVGStroke from "./components/animateSVGStroke.vue";
import animateSVGStrokeStagger from "./components/animateSVGStrokeStagger.vue";
import animatePin from "./components/animatePin.vue";
</script>

<template>
  <div class="background">
    <hero />
    <animatePositionXY />
    <animateText />
    <animateChangeColor />
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
