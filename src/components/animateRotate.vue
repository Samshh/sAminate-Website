<script setup>
import { onMounted } from "vue";
import { gsap } from "gsap";
import { ScrollTrigger } from "gsap/ScrollTrigger";
import { TextPlugin } from "gsap/TextPlugin";
import { animateRotate } from "saminate";

gsap.registerPlugin(ScrollTrigger);
gsap.registerPlugin(TextPlugin);
onMounted(() => {
  animateRotate(
    ".scrubwrapper",
    360,
    ".animateRotate",
    2,
    0,
    "power1.inOut",
    "top center",
    "bottom center",
    "play reverse play reverse",
    false,
    true
  );
});
</script>

<template>
  <div class="animateRotate">
    <div class="scrubwrapper">
      <h1 class="animateRot">animateRotate</h1>
      <p class="animateRotDesc">rotate an element</p>
    </div>
  </div>
</template>

<style scoped>
.scrubwrapper {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  overflow: hidden;
}
.animateRotate {
  display: flex;
  justify-content: center;
  align-items: center;
  overflow: hidden;
  height: 100vh;
}
.animateRot {
  font-size: clamp(1rem, 5vw, 3rem);
  color: #e7e7e7;
  user-select: none;
  margin: 0;
  text-align: center;
}
.animateRotDesc {
  font-size: clamp(0.8rem, 3vw, 1.5rem);
  color: #e7e7e7;
  user-select: none;
  margin: 0;
  text-align: center;
}
</style>
