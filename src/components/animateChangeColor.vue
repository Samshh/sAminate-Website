<script setup>
import { onMounted } from "vue";
import { gsap } from "gsap";
import { ScrollTrigger } from "gsap/ScrollTrigger";
import { TextPlugin } from "gsap/TextPlugin";
import { animateChangeColor } from "saminations";

gsap.registerPlugin(ScrollTrigger);
gsap.registerPlugin(TextPlugin);
onMounted(() => {
  animateChangeColor(
    ".animateCC",
    "#dc143c",
    ".animateChangeColor",
    1,
    0.5,
    "power1.inOut",
    "top center",
    "bottom center",
    "play reset play reset"
  );
});
</script>

<template>
  <div class="animateChangeColor">
    <h1 class="animateCC">animateChangeColor</h1>
    <p class="descSuggestion">animate the color change of an element</p>
  </div>
</template>

<style scoped>
.animateChangeColor {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  height: 100vh;
  overflow: hidden;
  width: 100vw;
}
.animateCC {
  font-size: clamp(1rem, 5vw, 3rem);
  color: #e7e7e7;
  user-select: none;
  margin: 0;
  text-align: center;
}
.descSuggestion {
  font-size: clamp(0.8rem, 3vw, 1.5rem);
  color: #e7e7e7;
  user-select: none;
  margin: 0;
  text-align: center;
}
</style>
