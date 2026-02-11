<script setup lang="ts">
  import pineapple_cat from '../assets/pixel_pineapple_cat.png';
</script>

<template>
  <footer class="footer">
    <img :src="pineapple_cat" alt="pineapple cat pfp" class="footer-photo"/>
    <p class="footer-text">
      © 2026 Kevin Sirantoine
      <br>All Rights Reserved
    </p>
  </footer>
</template>

<style lang="scss">
  .footer {
    display: flex;
    flex-direction: column;
    align-items: center;
    padding-top: clamp(7.5rem, 10vw, 10rem);
    padding-bottom: 2.5rem;
    gap: 0.5rem;
  }

  .footer-text {
    text-align: center;
    color: $lm_dim;
  }
  
  .footer-photo {
    width: 50px;
    height: 50px;
    transition: 150ms ease;
  }

  .footer-photo:hover {
    transform: scale(1.1);
  }
</style>