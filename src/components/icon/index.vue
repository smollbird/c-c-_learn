<script setup lang="ts">
const props = defineProps(["name"]);
</script>

<template>
  <i class="iconfont-default-style iconfont" :class="`icon-${props.name}`"></i>
</template>

<style scoped>
.iconfont-default-style {
  font-size: 28px;
}
</style>
