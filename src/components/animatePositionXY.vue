<script setup>
import { onMounted } from "vue";
import { gsap } from "gsap";
import { ScrollTrigger } from "gsap/ScrollTrigger";
import { TextPlugin } from "gsap/TextPlugin";
import { animatePositionX, animatePositionY } from "saminate";

gsap.registerPlugin(ScrollTrigger);
gsap.registerPlugin(TextPlugin);
onMounted(() => {
  animatePositionX(
    ".animateX",
    ".positionXY",
    "500",
    1,
    0,
    0,
    "power1.inOut",
    "top center",
    "bottom center",
    "play reset play reset"
  );
  animatePositionY(
    ".animateY",
    ".positionXY",
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
  <div class="positionXY">
    <div class="animatePositionX">
      <h1 class="animateX">animatePositionX</h1>
      <p class="descSuggestion">animate the position of an element in X-axis</p>
    </div>
    <div class="animatePositionY">
      <h1 class="animateY">animatePositionY</h1>
      <p class="descSuggestion">animate the position of an element in Y-axis</p>
    </div>
  </div>
</template>

<style scoped>
.positionXY {
  display: flex;
  justify-content: space-evenly;
  align-items: center;
  height: 100vh;
  overflow: hidden;
  width: 100vw;
}
.descSuggestion {
  font-size: clamp(0.8rem, 3vw, 1.5rem);
  color: #161616;
  user-select: none;
  margin: 0;
  text-align: center;
}
.animatePositionX,
.animatePositionY {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
}
.animateX,
.animateY {
  font-size: clamp(1rem, 5vw, 3rem);
  color: #161616;
  user-select: none;
  margin: 0;
  text-align: center;
}

@media (max-width: 1310px) {
  .positionXY {
    flex-direction: column;
  }
}
</style>
