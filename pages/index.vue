<template>
  <default>
    <div @wheel.prevent @touchmove.prevent @scroll.prevent>
      <Position />
      <WaitList />
    </div>
  </default>
</template>

<script setup lang="ts">
if (window?.Telegram) {
  window.Telegram.WebApp.disableVerticalSwipes();
  window.Telegram.WebApp.expand();
}
</script>
