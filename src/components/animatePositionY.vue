<script setup>
import { onMounted } from "vue";
import { gsap } from "gsap";
import { ScrollTrigger } from "gsap/ScrollTrigger";
import { TextPlugin } from "gsap/TextPlugin";
import { animatePositionY } from "saminations";

gsap.registerPlugin(ScrollTrigger);
gsap.registerPlugin(TextPlugin);
onMounted(() => {
  animatePositionY(
    ".animateY",
    ".animatePositionY",
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
  <div class="animatePositionY">
    <h1 class="animateY">animatePositionY</h1>
    <p class="descSuggestion">animate the position of an element in Y-axis</p>
  </div>
</template>

<style scoped>
.descSuggestion {
  font-size: clamp(0.8rem, 3vw, 1.5rem);
  color: #161616;
  user-select: none;
  text-align: center;
  margin: 0;
}
.animatePositionY {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  height: 100vh;
  overflow: hidden;
  width: 100vw;
}
.animateY {
  font-size: clamp(1rem, 5vw, 3rem);
  color: #161616;
  user-select: none;
  text-align: center;
  margin: 0;
}
</style>
