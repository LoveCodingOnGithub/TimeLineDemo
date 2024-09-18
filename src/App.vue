<script setup>
import { onMounted, ref } from "vue";
import TimeLine from "./components/TimeLine/src/index.vue";

const timelineRef = ref();

const zoomIndex = ref(0);

onMounted(() => {
  setInterval(() => {
    timelineRef.value.setTime(Date.now());
  }, 1000);
});
</script>

<template>
  <TimeLine
    ref="timelineRef"
    :init-time="Date.now()"
    :init-zoom-index="zoomIndex"
    style="height: 70px"></TimeLine>
</template>

<style lang="less"></style>
