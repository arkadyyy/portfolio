<script setup lang="ts"></script>

<template>
  <div class="container">
    <div>
      <img class="img" :src="'../../public/about-me.svg'" />
      <div class="text_container">
        <h1 class="header">About me</h1>
        <p class="text">
          Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do
          eiusmod tempor incididunt ut labore et dolore magna aliqua. Lacus sed
          viverra tellus in hac. Aliquam eleifend mi in nulla posuere
          sollicitudin aliquam. Turpis in eu mi bibendum. Sit amet porttitor
          eget dolor morbi non arcu. Nisl pretium fusce id velit ut tortor
          pretium viverra suspendisse. Habitasse platea dictumst vestibulum
          rhoncus est pellentesque elit ullamcorper. Egestas congue quisque
          egestas diam. Diam maecenas ultricies mi eget.
        </p>
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
.text_container {
  background-color: #fff;
  border: 1px solid #272828;
  width: 90%;
  height: 50%;
  position: absolute;
  top: 3rem;
  z-index: 99;
  right: -200px;
  padding: 3rem;
}
.header {
  color: #272828;
  font-family: "Julius Sans One", sans-serif;
  font-weight: bold;
  margin-bottom: 2rem;
}
.text {
  color: #272828;
  font-family: "Julius Sans One", sans-serif;
}

.img {
  width: 800px;
  height: 800px;
  object-fit: contain;
  z-index: 99;
  right: 15rem;
  position: relative;
}
</style>
