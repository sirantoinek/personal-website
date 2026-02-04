<template>
  <ul class="bullet-list">
    <slot />
  </ul>
</template>

<style lang="scss" scoped>
  .bullet-list {
    padding-left: clamp(1.5rem, 2vw, 2rem);
    text-align: start;
  }

  :slotted(li) {
    margin-top: 0.35rem;
  }
</style>