<script setup lang="ts"></script>

<template>
  <div class="progress">
    <span class="start-time">0:00</span>
    <div class="bar">
      <p></p>
    </div>
    <span class="end-time">3:46</span>
  </div>
</template>

<style scoped lang="less">
.progress {
  margin: 10px 0;
  display: flex;
  align-items: center;
  height: 100%;
  width: 100%;
  font-size: 12px;
  font-weight: bold;
  box-sizing: border-box;
  .bar {
    --width:50px;
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
