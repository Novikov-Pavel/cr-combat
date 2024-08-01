<template>
  <default>
    <Position />sdk
    <WaitList />
  </default>
</template>

<script setup lang="ts">
import { initSwipeBehavior } from "@telegram-apps/sdk";

const [swipeBehavior] = initSwipeBehavior();

swipeBehavior.disableVerticalSwipe();
</script>

<style>
.scrollable-element {
  overflow-y: scroll;
}
</style>
