<script setup lang="ts">
import Greeting from "@/components/Home/Greeting.vue";
import MySkills from "@/components/Home/MySkills.vue";
import MyProjects from "@/components/Home/MyProjets.vue";
import Contact from "@/components/Home/Contact.vue";
import AboutMe from "@/components/Home/AboutMe.vue";
</script>

<template>
  <div class="container">
    <Greeting />
    <AboutMe />
    <MySkills />
    <MyProjects />
    <Contact />
  </div>
</template>

<style scoped>
.container {
  background-color: #272828;
  overflow-x: hidden;
}
</style>
