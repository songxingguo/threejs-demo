<template>
  <div ref="vrDom">
  </div>
</template>

<script setup>
import { ref, onMounted } from "vue";
import init from "./webxr_vr_sandbox";
const vrDom = ref(null);
onMounted(() => {
  const { renderer } = init();
  vrDom.value.appendChild(renderer.domElement);
});
</script>

<style>
</style>
