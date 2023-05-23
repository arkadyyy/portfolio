<script setup lang="ts">
import Button from "../Button.vue";
</script>

<template>
  <div class="container">
    <img class="img2" :src="'../../public/blob.svg'" />
    <div class="text_container">
      <h1 class="header">Arkady likovizki</h1>
      <h3 class="subheader1">a passionate full-stack developer</h3>
      <h3 class="subheader2">With a keen eye for design</h3>
      <Button :text="'read more'" />
    </div>
    <div>
      <div class="blob_container">
        <svg viewBox="0 0 200 200" xmlns="http://www.w3.org/2000/svg">
          <path
            fill="#E3F5E6"
            d="M49.1,-72.3C60.1,-59.6,63.1,-40.5,67.4,-23C71.6,-5.4,77.2,10.8,72.9,23.6C68.6,36.5,54.6,46.1,40.8,58.1C27,70.1,13.5,84.5,-1,85.8C-15.4,87.1,-30.8,75.4,-46.1,63.9C-61.4,52.3,-76.5,41.1,-79,27.1C-81.5,13.2,-71.4,-3.3,-63.5,-18.5C-55.6,-33.6,-50,-47.3,-39.8,-60.3C-29.5,-73.2,-14.8,-85.5,2.1,-88.4C19.1,-91.3,38.1,-85,49.1,-72.3Z"
            transform="translate(100 100)"
          />
        </svg>
      </div>
      <img class="img" :src="'../../public/hand_coding.svg'" />
      <!-- <X /> -->
    </div>
  </div>
</template>

<style scoped>
.container {
  background-color: #272828;
  height: 100vh;
  display: flex;
  align-items: center;
  justify-content: center;
  width: 100vw;
  overflow: hidden;
}

.text_container {
  display: flex;
  flex-direction: column;
  /* background-color: red; */
  background-color: #fff;
  border: 1px solid #272828;
  height: 60vh;
  width: 30%;
  position: relative;
  left: 1rem;
  padding: 2rem;
}
.blob_container {
  /* background-color: green; */
  position: absolute;
  top: 10px;
  width: 100vh;
  height: 50vw;
  left: 100px;
}
.img {
  width: 800px;
  height: 800px;
  object-fit: contain;
  z-index: 99;
  position: relative;
  left: 100px;
}
.img2 {
  position: absolute;
  width: 110%;
  height: 110%;
  left: -40%;
  top: -40%;
}
.header {
  color: #272828;
  font-family: "Julius Sans One", sans-serif;
  font-size: 70px;
  width: 50%;
  margin-bottom: 4%;
}
.subheader1 {
  color: #272828;
  font-family: "Julius Sans One", sans-serif;
  font-size: 30px;
  margin-bottom: 3%;
  width: 80%;
}
.subheader2 {
  color: #272828;
  font-family: "Jua", sans-serif;

  font-size: 20px;
}
svg#freepik_stories-hand-coding:not(.animated) .animable {
  opacity: 0;
}
svg#freepik_stories-hand-coding.animated #freepik--hand-2--inject-11 {
  animation: 3s Infinite linear shake;
  animation-delay: 0.5s;
}
svg#freepik_stories-hand-coding.animated #freepik--hand-1--inject-11 {
  animation: 6s Infinite linear shake;
  animation-delay: 0s;
}
@keyframes shake {
  10%,
  90% {
    transform: translate3d(-1px, 0, 0);
  }
  20%,
  80% {
    transform: translate3d(2px, 0, 0);
  }
  30%,
  50%,
  70% {
    transform: translate3d(-4px, 0, 0);
  }
  40%,
  60% {
    transform: translate3d(4px, 0, 0);
  }
}
.animator-hidden {
  display: none;
}
</style>
