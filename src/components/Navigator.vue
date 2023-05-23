<script setup lang="ts">
import code_icon from "../assets/icons/code.png";
import contact from "../assets/icons/contact.png";
import about_me from "../assets/icons/about-me.png";
import menu from "../assets/icons/menu.png";
const btnArray = [code_icon, contact, about_me, menu];
</script>

<template>
  <div class="container">
    <button v-for="img in btnArray">
      <img v-bind:src="img" />
    </button>
  </div>
</template>

<style scoped>
.container {
  background-color: #ffffff99;
  border-radius: 5px;
  width: 30%;
  left: 33%;
  position: sticky;
  bottom: 5vh;
  z-index: 999;
  height: 60px;
  border: 1px solid #272828;
  box-shadow: 2px 2px 2px #00000070;
  display: flex;
  align-items: center;
  justify-content: space-around;
}

img {
  width: 20px;
  height: 20px;
  object-fit: contain;
}
</style>
