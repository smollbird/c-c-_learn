<template>
  <div class="music-panel">
    <FirstStatus
      @changeStatus="changeStatus"
      v-if="status === 'first'"
    ></FirstStatus>
    <SecondStatus
      songer="Westlife"
      :time="226"
      title="Nothing's Gonna Change My Love For You"
      @changeStatus="changeStatus"
      v-if="status === 'second'"
    ></SecondStatus>
    <!-- <ThirdStatus v-if="status === 'third'" @changeStatus="changeStatus"></ThirdStatus> -->
  </div>
</template>

<script setup lang="ts">
import {  ref } from "vue";
import type { Ref } from "vue";
import FirstStatus from "./views/FirstStatus.vue";
import SecondStatus from "./views/SecondStatus.vue";
// import ThirdStatus from "./views/ThirdStatus.vue";

const status: Ref<string> = ref("first");
// const statusStyle:ComputedRef<number> = computed(()=>status.value === 'first' ? 0 : 1)
const changeStatus = function (value: string) {
  status.value = value;
  console.log("hhh", value);
};
</script>

<style lang="less" scoped>
.music-panel {
  height: 92px;
  width: 200px;
  position: absolute;
  top: 0;
  right: 0;
  // opacity: v-bind(statusStyle);
  // background-color: #212132;
  // color: #fff;
}
</style>
