<script lang="ts">
import { ref, computed, onMounted, type Ref } from "vue";

const skillss = [
  "React",
  "Javascript",
  "Typescript",
  "SQL",
  "React native",
  "Python",
  "AWS",
];
const skills = ref([
  "React",
  "Javascript",
  "Typescript",
  "SQL",
  "React native",
  "Python",
  "AWS",
]);

const container = ref(null);

onMounted(() => {
  createInfiniteScroll(container.value);
  startAutoScroll(container.value);
});

function createInfiniteScroll(container) {
  const content = container.querySelector(".content");
  const clonedContent = content.cloneNode(true);

  container.appendChild(clonedContent);

  container.addEventListener("scroll", () => {
    if (container.scrollLeft >= container.scrollWidth - container.clientWidth) {
      container.scrollLeft = 0;
    }
  });
}

function startAutoScroll(container) {
  const scrollInterval = setInterval(() => {
    container.scrollLeft += 1;
  }, 10);
}
</script>

<template>
  <div class="container">
    <div>
      <img class="img" :src="'../../public/book-lover-animate.svg'" />
      <div class="scrolling-container">
        <div class="content">
          <div
            class="card"
            v-for="(item, index) in [1, 2, 3, 4, 5, 6, 7]"
            :key="index"
          >
            <h2>{{ item }}</h2>
          </div>
        </div>
        <!-- <li class="card">s</li>
        <li class="card">s</li>
        <li class="card">s</li>
        <li class="card">s</li>
        <li class="card">s</li>
        <li class="card">s</li>
        <li class="card">s</li>
        <li class="card">s</li>
        <li class="card">s</li> -->
      </div>
    </div>
  </div>
</template>

<style scoped>
.container {
  height: 100vh;
  display: flex;
  align-items: center;
  justify-content: center;
  flex-direction: column;
}

.scrolling-container {
  width: 100vw;
  /* background-color: red; */
  height: 30vh;
  position: absolute;
  overflow-x: scroll;
  top: 20rem;
  z-index: 999;
  display: flex;
  margin: 4px, 4px;
  padding: 4px;
  /* background-color: #08c708; */
  /* width: 300px; */
  overflow-x: auto;
  overflow-y: hidden;
  white-space: nowrap;
  width: 100%;
  white-space: nowrap;
}
.content {
  width: 200%;
}

.content > div {
  flex: 0 0 auto;
  width: 50%;
  padding: 10px;
  background-color: #fff;
  border: 1px solid #272828;
  margin-right: 3rem;
  height: 300px;
  width: 200px;
  display: inline-block;
}

.card {
  display: inline-block;
  background-color: #fff;
  border: 1px solid #272828;
  margin-right: 3rem;
  height: 300px;
  width: 200px;
}

.img {
  width: 800px;
  height: 800px;
  object-fit: contain;
  z-index: 99;
  position: relative;
}

/* Hide scrollbar for Chrome, Safari and Opera */
.scrolling-container::-webkit-scrollbar {
  display: none;
}

/* Hide scrollbar for IE, Edge and Firefox */
.scrolling-container {
  -ms-overflow-style: none; /* IE and Edge */
  scrollbar-width: none; /* Firefox */
}
</style>
