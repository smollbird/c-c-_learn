<template>
  <div class="music-first_status" @mouseenter="handler">
    <Icon name="tinggeshiqu" />
  </div>
</template>
<script setup lang="ts">
import Icon from "@/components/icon/index.vue";
const emits = defineEmits(['changeStatus']);
const handler = ()=>{
  emits('changeStatus','second');
}
</script>

<style lang="less" scoped>
.music-first_status {
  display: flex;
  justify-content: center;
  align-items: center;
  width: 30px;
  height: 30px;
  position: absolute;
  right: 10px;
  top: 10px;
  border-radius: 50%;
  animation: rotate 2s linear infinite;
  overflow: hidden;
  cursor: pointer;
}
// 旋转动画
@keyframes rotate {
  0% {
    transform: rotate(0deg);
  }
  100% {
    transform: rotate(360deg);
  }
}
</style>
