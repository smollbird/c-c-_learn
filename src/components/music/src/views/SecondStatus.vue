<template>
  <div class="music-second_status">
    <div class="song_info">
      <div class="portrait">
        <img src="@/assets/portrait.jpg" alt="" />
      </div>
      <div class="song_name">
        <p>Nothing's Gonna Change My Love For You</p>
        <p>Westlife</p>
      </div>
    </div>

    <SongProgress></SongProgress>

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
</script>

<style lang="less" scoped>
.music-second_status {
  .song_info {
    display: flex;
    .portrait {
      img {
        margin-right: 10px;
        width: 50px;
        height: 50px;
        border-radius: 50%;
        vertical-align: bottom;
      }
    }
    .song_name {
      p {
        width: 140px;
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
  }
}
</style>
