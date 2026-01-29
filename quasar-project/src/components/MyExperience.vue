<script setup lang="ts">
  
</script>

<template>
  <div class="myExperience">
    <h1 class="header-text">
      My Background
    </h1>
  </div>
</template>

<style lang="scss">
  .myExperience {
    display: flex;
    flex-direction: column;
    justify-content: flex-start;
	  position: relative;
    gap: 2rem;
    margin-top: 5rem;
  }

  .header-text {
    display: flex;
    font-size: clamp(2rem, 4vw, 4rem);
    margin-top: 2.5rem;
    margin-bottom: 0px;
    line-height: 1;
    gap: 0.25em;
    flex-wrap: wrap;
    white-space: nowrap;
  }

  @media (max-width: 730px) {
    .myExperience {
      margin-top: 2.5rem;
    }
  }

  @media (min-width: 1200px) {
    .myExperience {
      margin-top: 10rem;
      transition: 150ms;
    }
  }
</style>