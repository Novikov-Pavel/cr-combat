<template>
  <default>
    <Position />
    <WaitList />
  </default>
</template>

<script setup lang="ts">
if (window?.Telegram) {
  window.Telegram.WebApp.disableVerticalSwipes();
  window.Telegram.WebApp.viewportStableHeight = 768;
}
</script>

<style>
.scrollable-element {
  overflow-y: scroll;
}
</style>
