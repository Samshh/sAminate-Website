<script setup>
import { onMounted } from "vue";
import { gsap } from "gsap";
import { ScrollTrigger } from "gsap/ScrollTrigger";
import { TextPlugin } from "gsap/TextPlugin";
import {
  animateBgChangeColor,
  animateChangeColor,
  animateOpacityChange,
} from "saminate";

gsap.registerPlugin(ScrollTrigger);
gsap.registerPlugin(TextPlugin);
onMounted(() => {
  animateBgChangeColor(".background", "#161616", ".outerCCWRAP", 0.5);
  animateChangeColor(
    ".animateCC",
    "#dc143c",
    ".outerCCWRAP",
    1,
    0.5,
    "power1.inOut",
    "top center",
    "bottom center",
    "play reset play reset"
  );
  animateOpacityChange(
    ".animateOpacity",
    ".outerCCWRAP",
    3,
    0,
    1,
    "power1.inOut",
    "top center",
    "bottom center",
    "play reset play reset"
  );
});
</script>

<template>
  <div class="outerCCWRAP">
    <div class="changeColorWrap">
      <div class="animateBgChangeColor">
        <h1 class="animateBg">animateBgChangeColor</h1>
        <p class="descSuggestion">animate the change in background-color</p>
      </div>
      <div class="animateChangeColor">
        <h1 class="animateCC">animateChangeColor</h1>
        <p class="descSuggestion">animate the color change of an element</p>
      </div>
    </div>
    <div class="animateOpacityChange">
      <h1 class="animateOpacity">animateOpacityChange</h1>
      <p class="descSuggestion">animate the change in opacity of an element</p>
    </div>
  </div>
</template>

<style scoped>
.outerCCWRAP {
  height: 100vh;
  width: 100vw;
  display: flex;
  flex-direction: column;
  justify-content: space-evenly;
}
.changeColorWrap {
  display: grid;
  grid-template-columns: 1fr 1fr;
}
.animateBgChangeColor,
.animateChangeColor,
.animateOpacityChange {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  overflow: hidden;
}
.animateBg,
.animateCC,
.animateOpacity {
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

@media (max-width: 1440px) {
  .changeColorWrap {
    display: flex;
    flex-direction: column;
    justify-content: space-evenly;
    height: 50vh;
  }
  .outerCCWRAP{
    justify-content: start;
  }
}

</style>
