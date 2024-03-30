<script setup>
import { onMounted } from "vue";
import { gsap } from "gsap";
import { ScrollTrigger } from "gsap/ScrollTrigger";
import { TextPlugin } from "gsap/TextPlugin";
import { animateScale } from "saminate";

gsap.registerPlugin(ScrollTrigger);
gsap.registerPlugin(TextPlugin);
onMounted(() => {
  animateScale(
    ".animateSc",
    550,
    ".animateScale",
    7,
    1,
    "power1.inOut",
    "top center",
    "bottom center",
    "play reset play reset",
  );
});
</script>

<template>
  <div class="animateScale">
    <h1 class="animateSc">animateScale</h1>
    <p class="descSuggestion">animate the scale of an element</p>
    <p class="descSuggestion">try scrub with this, and create something amazing!</p>
  </div>
</template>

<style scoped>
.animateScale {
  display: flex;
  justify-content: center;
  align-items: center;
  height: 100vh;
  overflow: hidden;
  flex-direction: column;
}
.animateSc {
  font-size: clamp(1rem, 5vw, 3rem);
  color: #e7e7e7;
  user-select: none;
  margin: 0;
}
.descSuggestion {
  font-size: clamp(0.8rem, 2vw, 1.5rem);
  color: #e7e7e7;
  user-select: none;
  margin: 0;
  mix-blend-mode: difference;
  text-align: center;
}
</style>
