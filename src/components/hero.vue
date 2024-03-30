<script setup>
import { onMounted, computed } from "vue";
import { gsap } from "gsap";
import { Icon } from "@iconify/vue";

let text = "sAminations";
let chars = computed(() => text.split(""));

onMounted(() => {
  let spans = document.querySelectorAll(".mainHeroTxt span");

  spans.forEach((span, i) => {
    gsap.from(span, {
      duration: 1,
      delay: i * 0.1,
      opacity: 0,
      ease: "power1.inOut",
    });
  });

  gsap.to(".subHeroTxt", {
    opacity: 1,
    duration: 1,
    delay: 1.5,
    ease: "power1.inOut",
  });
});
</script>

<template>
  <div class="hero">
    <h1 class="mainHeroTxt">
      <span v-for="(char, i) in chars" :key="i">{{ char }}</span>
    </h1>
    <p class="subHeroTxt">a GSAP animations <a class="links" target="_blank" href="https://github.com/Samshh/sAminations">library</a> for JavaScript</p>
    <p class="subHeroTxt">by <a class="links" target="_blank" href="https://samshh.netlify.app/">samshh.</a></p>
  </div>
</template>

<style scoped>
.hero {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  height: 100vh;
  overflow: hidden;
  width: 100vw;
}
.mainHeroTxt {
  font-size: clamp(2.5rem, 5vw, 6rem);
  color: #161616;
  user-select: none;
  margin: 0;
}
.subHeroTxt {
  font-size: clamp(0.8rem, 5vw, 1.5rem);
  color: #161616;
  user-select: none;
  margin: 0;
  opacity: 0;
  text-align: center;
}
.links {
  color: #161616;
  text-decoration: underline;
}
</style>
