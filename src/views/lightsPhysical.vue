<template>
  <div ref="lightsPhysicalDom">
  </div>
</template>

<script setup>
import { ref, onMounted } from "vue";
import init from "./webgl_lights_physical";
const lightsPhysicalDom = ref(null);
onMounted(() => {
  const { renderer, stats } = init();
  lightsPhysicalDom.value.appendChild(renderer.domElement);
  lightsPhysicalDom.value.appendChild(stats.dom);
});
</script>

<style>
</style>
