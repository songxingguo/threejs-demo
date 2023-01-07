<template>
  <div ref="screenDom"></div>
</template>
<script setup>
import { ref, onMounted } from "vue";
import ThreeFactory from "./ThreeFactory";
let screenDom = ref(null);
onMounted(() => {
  const threeFactory = new ThreeFactory();
  const { scene, camera, renderer } = threeFactory.init();
  screenDom.value.appendChild(renderer.domElement);
  function render() {
    renderer.render(scene, camera);
    // 渲染下一帧的时候调用render函数
    requestAnimationFrame(render);
  }
  render();
});
</script>

