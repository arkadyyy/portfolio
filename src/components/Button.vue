<script setup lang="ts">
import { defineProps } from "vue";

const props = defineProps(["text"]);
</script>

<template>
  <button class="btn">
    {{ props.text }}
  </button>
</template>

<style scoped>
.btn {
  background-color: white;
  padding: 0.7rem;
  border-radius: 4px;
  display: flex;
  justify-content: center;
  align-items: center;
  color: black;
  font-family: "Julius Sans One", sans-serif;
  width: 150px;
  cursor: pointer;
  position: relative;
  top: 50px;
}
</style>
