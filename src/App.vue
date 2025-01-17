<script setup>
import { ref } from "vue";
import { useRouter } from "vue-router";

const router = useRouter();

function handleClick(name) {
  router.push({ name: name });
}
</script>

<template>
  <div>
    <el-button plain @click="handleClick('home')">home</el-button>
    <el-button plain @click="handleClick('about')">about</el-button>
  </div>
  <RouterView />
</template>

<style scoped></style>
