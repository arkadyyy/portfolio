<script setup lang="ts"></script>

<template>
  <div class="container">
    <div>
      <img class="img" :src="'../../public/gallery.svg'" />
    </div>
  </div>
</template>
<style scoped>
.container {
  height: 120vh;
  display: flex;
  align-items: center;
  justify-content: center;
  flex-direction: column;
}

.img {
  width: 800px;
  height: 800px;
  object-fit: contain;
  z-index: 99;
  position: relative;
}
</style>
