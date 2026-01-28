<script setup lang="ts">
  import NavBar from 'components/NavBar.vue';
  import AboutMe from 'components/AboutMe.vue';
  import AppFooter from 'components/AppFooter.vue';
</script>

<template>
  <main class="main">
    <NavBar/>
    <AboutMe/>
    <AppFooter/>
  </main>
</template>

<style scoped>
	.main {
		height: 1500px;
    width: 90%;
    max-width: fit-content;
    justify-content: center;
    margin-left: auto;
    margin-right: auto;
    padding-left: 2rem;
    padding-right: 2rem;
    transition: 150ms;
	}

  @media (max-width: 600px) {
    .main {
      width: 100%;
    }
  }

  @media (min-width: 1200px) {
    .main {
      width: 85%;
    }
  }
</style>