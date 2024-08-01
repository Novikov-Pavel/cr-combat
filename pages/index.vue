<template>
  <default>
    <Position />213
    <WaitList />
  </default>
</template>

<script setup lang="ts">
window?.Telegram && window.Telegram.WebApp.disableVerticalSwipes();
</script>

<style>
.scrollable-element {
  overflow-y: scroll;
}
</style>
