<template>
  <default>
    <div @wheel.passive.prevent.stop>
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
