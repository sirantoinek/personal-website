<script setup lang="ts">
  import profileImage1 from '../assets/profile_photo1.png';
  import profileImage2 from '../assets/profile_photo2.png';
</script>

<template>
  <div class="aboutMe">
    <h1 class="title-text">
      <span>Hi, I'm</span>
      <span>
        <span 
          v-for="(char, index) in 'Kevin Sirantoine'" 
          :key="index"
          :style="{ animationDelay: `${index * .1}s` }"
          class="wave-char"
        >
          {{ char === ' ' ? '\u00A0' : char }} <!-- \u00A0 is a non-breaking space -->
        </span>
      </span>
    </h1>
    <span class="desc">
      <span>
        <p class="desc-text">
          A software developer and computer enthusiast passionate about building practical and efficient applications.
        </p>
        <p class="desc-text">
          I enjoy exploring new technologies, solving problems, and finding creative solutions.
        </p>
        <p class="desc-text">
          When I'm not coding, I'm usually tinkering with computers or enjoying the outdoors.
        </p>
      </span>
      <div class="photo-frame">
        <img :src="profileImage1" alt="profile image 1" class="photo"/>
        <img :src="profileImage2" alt="profile image 2" class="photo"/>
      </div>
    </span>
  </div>
</template>

<style lang="scss">
  .aboutMe {
    display: flex;
    flex-direction: column;
    justify-content: flex-start;
		position: relative;
    margin-top: .75rem;
    gap: 1.5rem;
	}

  .title-text {
    display: flex;
    font-size: clamp(2.5rem, 5vw, 5rem);
    margin-top: 2.5rem;
    margin-bottom: 0px;
    line-height: 1;
    gap: 0.25em;
    flex-wrap: wrap;
    white-space: nowrap;
  }

  .wave-char {
    display: inline-block;
    animation: waveText 2s ease-in-out infinite;
  }

  .desc {
    display: flex;
    flex-direction: column;
    align-items: flex-start;
    flex-wrap: wrap;
    gap: 1rem;
  }

  .desc-text {
    font-size: clamp(1.2rem, 1.5vw, 1.5rem);
    margin-bottom: 1rem;
    max-width: 915px;
  }

  .photo-frame {
    display: grid;
    grid-template-areas: "stack";
    max-width: 200px;
    border-radius: .5rem;
    overflow: hidden;
    transition: 150ms ease;
  }

  .photo-frame:hover {
    transform: scale(1.05);
  }

  .photo {
    width: 100%;
    grid-area: stack;
    animation: crossFadePhotos 15s infinite ease;
  }

  .photo:nth-child(2) {
    animation-delay: -7.5s;
  }

  @media (min-width: 730px) {
    .desc {
      flex-direction: row;
      flex-wrap: nowrap;
    }
  }

  @media (min-width: 1200px) {
    .photo-frame {
      max-width: 300px;
      margin-left: 5rem;
    }
  }

  @keyframes waveText {
    0%, 100% { transform: translateY(0); }
    50% { transform: translateY(-.06em); }
  }

  @keyframes crossFadePhotos {
    0%, 40% { opacity: 1; }
    45%, 80% { opacity: 0; }
    85%, 100% { opacity: 1; }
  }
</style>