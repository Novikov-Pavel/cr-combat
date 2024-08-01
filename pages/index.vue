<template>
  <default>
    <div class="scrollable-element" @touchstart="preventCollapse">
      <Position />
      <WaitList />
    </div>
  </default>
</template>

<script setup lang="ts">
function ensureDocumentIsScrollable() {
  const isScrollable =
    document.documentElement.scrollHeight > window.innerHeight;
  if (!isScrollable) {
    document.documentElement.style.setProperty(
      "height",
      "calc(100vh + 1px)",
      "important"
    );
  }
}
function preventCollapse() {
  if (window.scrollY === 0) {
    window.scrollTo(0, 1);
  }
}

// window.addEventListener("load", ensureDocumentIsScrollable);
</script>

<style>
.scrollable-element {
  overflow-y: scroll;
}
</style>
