<script setup>
import { onMounted } from "vue";
import { gsap } from "gsap";
import { ScrollTrigger } from "gsap/ScrollTrigger";
import { TextPlugin } from "gsap/TextPlugin";
import { animateBgChangeColor } from "saminations";

gsap.registerPlugin(ScrollTrigger);
gsap.registerPlugin(TextPlugin);
onMounted(() => {
  animateBgChangeColor(
    ".background",
    "#161616",
    ".animateBgChangeColor",
    .5
  );
});
</script>

<template>
  <div class="animateBgChangeColor">
    <h1 class="animateBg">animateBgChangeColor</h1>
    <p class="descSuggestion">animate the change in background-color</p>
  </div>
</template>

<style scoped>
.animateBgChangeColor {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  height: 100vh;
  overflow: hidden;
  widows: 100vw;
}
.animateBg {
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
