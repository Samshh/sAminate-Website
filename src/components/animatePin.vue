<script setup>
import { onMounted } from "vue";
import { gsap } from "gsap";
import { ScrollTrigger } from "gsap/ScrollTrigger";
import { TextPlugin } from "gsap/TextPlugin";
import { animatePin, animateChangeColor } from "saminations";

gsap.registerPlugin(ScrollTrigger);
gsap.registerPlugin(TextPlugin);
onMounted(() => {
  animateChangeColor(".copyright", "#e7e7e7", ".animateBgChangeColor", 0.5);
  animatePin(
    ".thePinned",
    ".elementUnPinned",
    "center center",
    "center center",
    false,
    false,
    "play none none none",
    ".lastpin"
  );
});
</script>

<template>
  <div class="animatePin">
    <div class="thePinned">
      <h1 class="animatePinThis">animatePin</h1>
      <p class="animatePinThisDesc">pin an element</p>
      <p class="animatePinThisDesc">use display: grid;</p>
    </div>
    <div class="unpinned">
      <h1 class="elementUnPinned">your element here</h1>
      <h1 class="elementUnPinned">THANK</h1>
      <h1 class="elementUnPinned">YOU</h1>
      <h1 class="elementUnPinned">FOR</h1>
      <h1 class="elementUnPinned">USING</h1>
      <h1 class="elementUnPinned lastpin">MY LIBRARY :></h1>
    </div>
    <p class="copyright">© 2024 Samshh</p>
  </div>
</template>

<style scoped>
.copyright {
  position: fixed;
  bottom: 0;
  left: 50%;
  transform: translateX(-50%);
  color: #161616;
  font-size: clamp(0.5rem, 2vw, 1rem);
}
.animatePinThisDesc {
  font-size: clamp(0.8rem, 2vw, 1.5rem);
  color: #e7e7e7;
  user-select: none;
  margin: 0;
}
.thePinned {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
}
.animatePin {
  display: grid;
  grid-template-columns: 1fr 1fr;
  justify-content: center;
  align-items: start;
  height: auto;
  overflow: hidden;
  width: 100vw;
}
.animatePinThis,
.elementUnPinned {
  font-size: clamp(1rem, 5vw, 3rem);
  color: #e7e7e7;
  user-select: none;
  margin: 0;
}
.elementUnPinned {
  height: 30vh;
  display: flex;
  justify-content: center;
  align-items: center;
}
.unpinned {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
}
</style>
