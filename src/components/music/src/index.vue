<template>
  <div class="music-panel">
    <FirstStatus></FirstStatus>
    <SecondStatus></SecondStatus>
    <!-- <ThirdStatus></ThirdStatus> -->
  </div>
</template>

<script setup lang="ts">
import FirstStatus from "./views/FirstStatus.vue";
import SecondStatus from "./views/SecondStatus.vue";
// import ThirdStatus from "./views/ThirdStatus.vue";
</script>

<style lang="less" scoped>
.music-panel {
  height: 130px;
  width: 200px;
  position: absolute;
  top: 0;
  right: 0;
}
</style>
