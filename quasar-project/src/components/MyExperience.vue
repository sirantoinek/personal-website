<script setup lang="ts">
  
</script>

<template>
  <div class="myExperience">
    <h2 class="header-text">My Background</h2>
    <div class="info-cards">
      <div class="card" style="grid-area: card-1">
        <h3 class="subheader-text">Education</h3>
        <p class="card-text">
          University of Florida
        </p>
      </div>
      <div class="card" style="grid-area: card-2">
        <h3 class="subheader-text">Experience</h3>
      </div>
      <div class="card" style="grid-area: card-3">
        <h3 class="subheader-text">Certifications</h3>
      </div>
      <div class="card" style="grid-area: card-4">
        <h3 class="subheader-text">Skills</h3>
      </div>
    </div>
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
    font-size: clamp(2rem, 4vw, 4rem);
    margin-top: 2.5rem;
    margin-bottom: 0px;
    line-height: 1;
    white-space: nowrap;
  }

  .info-cards {
    display: grid;
    height: 800px;
    grid-auto-columns: 1fr;
    grid-auto-rows: 1fr;
    gap: 1rem;
    grid-template-areas: 
    "card-1 card-3"
    "card-2 card-2"
    "card-4 card-4";
  }

  .card {
    display: flex;
    flex-direction: column;
    padding: clamp(1rem, 2vw, 2rem);
    background-color: $lm-border;
    border-radius: .5rem;
    text-align: center;
    gap: clamp(1rem, 1.5vw, 1.5rem);
  }

  .subheader-text {
    font-size: clamp(1.75rem, 2.5vw, 2.5rem);
    font-weight: 300;
    margin: 0px;
    line-height: 1;
    white-space: nowrap;
  }

  .card-text {
    font-size: clamp(1rem, 1.25vw, 1.25rem);
    margin: 0px;
  }

  @media (max-width: 600px) {
    .info-cards {
      grid-template-areas: 
      "card-1"
      "card-2"
      "card-3"
      "card-4";
    }
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

    .info-cards {
      grid-template-columns: fit-content(200px) 1fr;
      grid-template-areas: 
      "card-1 card-2 card-2"
      "card-3 card-2 card-2"
      "card-4 card-4 card-4";
    }
  }
</style>