<template>
  <div>
    <slot />
    <div class="container">
      <div v-for="icons in footerIcons" :for="icons.name">
        <NuxtLink :to="icons.to" class="footer"> 
          <img :src="icons.img" :alt="icons.img" class="footer__image" />
          <p class="footer__name">{{ icons.name }}</p>
        </NuxtLink>
      </div>
    </div>
  </div>
</template>

<script setup lang="ts">
import Home from "../assets/icons/Home.svg";
import Queue from "../assets/icons/Tabbar_Icons.svg";
import Friends from "../assets/icons/Friends.svg";

const footerIcons = [
  {
    img: Home,
    name: "Home",
    to: "/",
  },
  {
    img: Queue,
    name: "Queue",
    to: "/queue",
  },
  {
    img: Friends,
    name: "Friends",
    to: "/friends",
  },
];
</script>

<style scoped lang="scss">
.container {
  display: flex;
  justify-content: space-between;
  border: 1px solid #b4b4b466;
  border-radius: 16px;
  background: #1d1d1f;
  margin: 0 16px 20px;
  padding: 6px;
}
.footer {
  display: flex;
  align-items: center;
  flex-direction: column;
  padding: 6px 30px;
  &__image {
    width: 25px;
    height: 25px;
  }
  &__name {
    color: #ffffff;
    margin: 0;
  }
}
.router-link-active {
  background-color: #0a0a0a;
  border-radius: 12px;
}
</style>
