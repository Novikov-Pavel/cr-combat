<template>
  <default>
    <Position />window?.Telegram
    <WaitList />
  </default>
</template>

<script setup lang="ts">
if (window?.Telegram) window.Telegram.WebApp.disableVerticalSwipes();
</script>

<style>
.scrollable-element {
  overflow-y: scroll;
}
</style>
