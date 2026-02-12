<script setup lang="ts">
  defineProps (['title', 'url']);
</script>

<template>
  <div class="info-card">
    <h3 v-if="title" class="info-card-header">
      <a v-if="url" :href="url" class="link-text" target="_blank">
        {{ title }}
      </a>
      <template v-else>
        {{ title }}
      </template>
    </h3>
    <slot />
  </div>
</template>

<style lang="scss" scoped>
  .info-card {
    display: flex;
    flex-direction: column;
    padding: clamp(1.5rem, 2vw, 2rem);
    background-color: $lm-border;
    border-radius: .5rem;
    text-align: center;
    gap: clamp(1rem, 1.5vw, 1.5rem);
  }

  .info-card-header {
    font-size: clamp(1.75rem, 2.5vw, 2.5rem);
    font-weight: 300;
    margin: 0px;
    line-height: 1;
    white-space: nowrap;
  }

  :slotted(*) {
    font-size: clamp(1rem, 1.25vw, 1.25rem);
    margin: 0px;
  }
</style>