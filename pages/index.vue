<template>
  <default>
    <div @touchstart="preventCollapse" class="scrollable-element">
      <Position />
      <WaitList />
    </div>
  </default>
</template>

<script setup lang="ts">
function ensureDocumentIsScrollable() {
  const isScrollable =
    document?.documentElement?.scrollHeight > window?.innerHeight;
  if (!isScrollable) {
    document?.documentElement?.style?.setProperty(
      "height",
      "calc(100vh + 1px)",
      "important"
    );
  }
}
ensureDocumentIsScrollable();

function preventCollapse(event) {
  if (window.scrollY === 0) {
    window.scrollTo(0, 1);
  }
}
</script>

<style>
.scrollable-element {
  overflow-y: scroll;
  height: 32rem;
  font-size: 6.25rem;
  border: 1px solid;
}
</style>
