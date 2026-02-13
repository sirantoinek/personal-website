<script setup lang="ts">
  import InfoCard from 'src/components/InfoCard.vue';
  import github_icon from '../assets/github_icon.png';
  import linkedin_icon from '../assets/linkedin_icon.png';
</script>

<template>
  <div class="contactMe">
    <h2 class="header-text">Contact Me</h2>
    <div class="contact-card">
      <InfoCard>
        <div class="contact-details">
          <a href="https://www.linkedin.com/in/sirantoinek" target="_blank" class="link-image">
            <img :src="linkedin_icon" alt="LinkedIn logo" class>
          </a>
          <a href="https://github.com/sirantoinek" target="_blank" class="link-image" style="border-radius: 50%; overflow: hidden;">
            <img :src="github_icon" alt="Github logo">
          </a>
        </div>
      </InfoCard>
    </div>
  </div>
</template>

<style lang="scss">
  .contactMe {
    display: grid;
    gap: 2rem;
    margin-top: 5rem;
  }

  .header-text {
    font-size: clamp(2rem, 4vw, 4rem);
    margin-top: 2.5rem;
    margin-bottom: 0px;
    line-height: 1;
    white-space: nowrap;
  }

  .contact-card {
    max-width: fit-content;
  }

  .contact-details {
    display: flex;
    flex-wrap: wrap;
    justify-content: center;
    gap: 2rem;
  }

  .link-image {
    display: flex;
    width: clamp(6.4rem, 15vw, 20rem);
    aspect-ratio: 1;
    transition: 150ms ease;
  }

  .link-image:hover {
    transform: scale(1.05);
  }

  @media (max-width: 730px) {
    .contactMe {
      margin-top: 2.5rem;
    }
  }

  @media (min-width: 1200px) {
    .contactMe {
      margin-top: 10rem;
      transition: 150ms;
    }
  }
</style>