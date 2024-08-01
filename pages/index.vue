<template>
  <default>
    <Position />
    <WaitList />
  </default>
</template>

<script setup lang="ts">
window?.Telegram && window.Telegram.WebApp.disableClosingConfirmation()
</script>

<style>
.scrollable-element {
  overflow-y: scroll;
}
</style>
