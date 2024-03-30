<script setup>
import { onMounted } from "vue";
import { gsap } from "gsap";
import { ScrollTrigger } from "gsap/ScrollTrigger";
import { TextPlugin } from "gsap/TextPlugin";
import { animatePositionX } from "saminations";

gsap.registerPlugin(ScrollTrigger);
gsap.registerPlugin(TextPlugin);
onMounted(() => {
  animatePositionX(
    ".animateX",
    ".animatePositionX",
    "500",
    1,
    0,
    0,
    "power1.inOut",
    "top center",
    "bottom center",
    "play reset play reset"
  );
});
</script>

<template>
  <div class="animatePositionX">
    <h1 class="animateX">animatePositionX</h1>
    <p class="descSuggestion">animate the position of an element in X-axis</p>
  </div>
</template>

<style scoped>
.descSuggestion {
  font-size: clamp(0.8rem, 3vw, 1.5rem);
  color: #161616;
  user-select: none;
  margin: 0;
  text-align: center;
}
.animatePositionX {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  height: 100vh;
  overflow: hidden;
  width: 100vw;
}
.animateX {
  font-size: clamp(1rem, 5vw, 3rem);
  color: #161616;
  user-select: none;
  margin: 0;
  text-align: center;
}
</style>
