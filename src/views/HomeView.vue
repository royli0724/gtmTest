<script setup>
import { ElMessage } from "element-plus";

function sendEvent() {
  ElMessage({
    message: "send home_event",
    type: "success",
    plain: true,
  });

  window.dataLayer = window.dataLayer || [];
  window.dataLayer.push({
    event: "home_event",
    data: "this is test data",
  });
}
</script>

<template>
  <div>home</div>
  <div class="bigBox">this is big box</div>
  <el-button plain @click="sendEvent()">sendEvent</el-button>
</template>

<style>
.bigBox {
  height: 150vh;
  display: flex;
  align-items: center;
  margin-bottom: 30px;
  background: rgb(239, 238, 237);
}
</style>
