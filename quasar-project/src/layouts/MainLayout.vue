<script setup lang="ts">
  import NavBar from 'components/NavBar.vue';
  import AboutMe from 'src/views/AboutMe.vue';
  import MyExperience from 'src/views/MyExperience.vue';
  import MyProjects from 'src/views/MyProjects.vue';
  import ContactMe from 'src/views/ContactMe.vue';
  import AppFooter from 'components/AppFooter.vue';
</script>

<template>
  <main class="main">
    <NavBar />
    <AboutMe />
    <MyExperience />
    <MyProjects />
    <ContactMe />
    <AppFooter />
  </main>
</template>

<style scoped>
	.main {
    width: 90%;
    max-width: 1500px;
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