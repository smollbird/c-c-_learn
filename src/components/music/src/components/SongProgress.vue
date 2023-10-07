<script setup lang="ts">
type Props = {
  time: number;
  currentTime: number;
  changeProgress?: () => void;
};
const props = defineProps<Props>();
const handleTimeFormat = function (time: number) {
  const s = time % 60;
  const m = Math.floor(time / 60);
  
  console.log(m,s,time);
  return `${m < 10 ? "0" + m : m}:${s < 10 ? "0" + s : s}`;
};
</script>

<template>
  <div class="progress">
    <span class="start-time">{{ handleTimeFormat(props.currentTime) }}</span>
    <div class="bar" :style="{ '--width': props.currentTime / props.time * 100 + '%' }">
      <p></p>
    </div>
    <span class="end-time">{{ handleTimeFormat(props.time) }}</span>
  </div>
</template>

<style scoped lang="less">
.progress {
  margin: 5px 0;
  display: flex;
  align-items: center;
  height: 100%;
  width: 100%;
  font-size: 12px;
  font-weight: bold;
  box-sizing: border-box;
  .bar {
    --width: 0px;
    height: 14px;
    width: 100%;
    background-color: #fff;
    border-radius: 12px;
    margin: 0 5px;
    p {
      background-color: #007bff;
      width: var(--width);
      height: 100%;
      border-radius: 12px;
    }
  }
}
</style>
