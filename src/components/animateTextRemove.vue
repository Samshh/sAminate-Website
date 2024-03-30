<script setup>
import { onMounted } from "vue";
import { gsap } from "gsap";
import { ScrollTrigger } from "gsap/ScrollTrigger";
import { TextPlugin } from "gsap/TextPlugin";
import { animateTextRemove } from "saminations";

gsap.registerPlugin(ScrollTrigger);
gsap.registerPlugin(TextPlugin);
onMounted(() => {
  animateTextRemove(
    ".animateTextRem",
    ".animateTextRemove",
    4,
    0,
    "power1.inOut",
    "top center",
    "bottom center",
    "play reset play reset"
  );
});
</script>

<template>
  <div class="animateTextRemove">
    <h1 class="animateTextRem">animateTextRemove</h1>
    <p class="descSuggestion">animate a text to remove</p>
  </div>
</template>

<style scoped>
.animateTextRemove {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  height: 100vh;
  overflow: hidden;
  width: 100vw;
}
.animateTextRem {
  font-size: clamp(1rem, 5vw, 3rem);
  color: #161616;
  user-select: none;
  margin: 0;
  text-align: center;
}
.descSuggestion {
  font-size: clamp(0.8rem, 3vw, 1.5rem);
  color: #161616;
  user-select: none;
  text-align: center;
  margin: 0;
}
</style>
