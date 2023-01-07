<template>
  <div class="about"
    ref="aboutDom">
  </div>
</template>

<script setup>
import { ref, onMounted } from "vue";
import init from "./gemo";
const aboutDom = ref(null);
onMounted(() => {
  const { renderer } = init();
  aboutDom.value.appendChild(renderer.domElement);
});
</script>

<style>
</style>
