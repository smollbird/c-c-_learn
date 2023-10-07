<template>
  <div class="music-second_status" @mouseleave="handler">
    <div class="song_info">
      <div class="portrait">
        <img src="@/assets/portrait.jpg" alt="" />
      </div>
      <div class="song_name">
        <p>{{ props.title }}</p>
        <p>{{ props.songer }}</p>
      </div>
    </div>

    <SongProgress
      :time="props.time"
      :currentTime="currentTime"
      @changeProgress="handleChangeProgress"
    ></SongProgress>

    <div class="music-control">
      <Icon name="suijibofang" />
      <Icon name="shangyiqu" />
      <Icon name="bofangzhong" />
      <!-- <Icon name="zanting" /> -->
      <Icon name="xiayiqu" />
      <Icon name="bofangduilie" />
    </div>
  </div>
</template>

<script setup lang="ts">
import Icon from "@/components/icon/index.vue";
import SongProgress from "../components/SongProgress.vue";
import { ref } from "vue";
import type { Ref } from "vue";
type Props = {
  songer: string;
  title: string;
  time: number;
};
const props = defineProps<Props>();
const emits = defineEmits(["changeStatus"]);
const currentTime: Ref<number> = ref(0);
const handler = () => {
  emits("changeStatus", "first");
};

// let time: Ref<number> = ref(0);
const handleChangeProgress = () => {};
</script>

<style lang="less" scoped>
.music-second_status {
  .song_info {
    display: flex;
    .portrait {
      img {
        margin-right: 10px;
        width: 32px;
        height: 32px;
        border-radius: 50%;
        vertical-align: bottom;
        animation: rotate 5s linear infinite;
      }
    }
    .song_name {
      font-size: 12px;
      p {
        width: 158px;
        overflow: hidden;
        text-overflow: ellipsis;
        white-space: nowrap;
      }
    }
  }

  .music-control {
    display: flex;
    align-items: center;
    justify-content: space-between;
    height: 28px;
    cursor: pointer;
  }
}
@keyframes rotate {
  0% {
    transform: rotate(0deg);
  }
  100% {
    transform: rotate(360deg);
  }
}
</style>
