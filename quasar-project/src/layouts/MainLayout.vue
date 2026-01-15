<script setup lang="ts">
  import NavBar from 'components/NavBar.vue';
</script>

<template>
  <main class="main">
    <NavBar/>
  </main>
</template>

<style scoped>
	.main {
		height: 1500px;
    justify-content: center;
    margin-left: 2%;
    margin-right: 2%;
    padding-left: 2rem;
    padding-right: 2rem;
	}

  @media (min-width: 600px) {
    .main {
      margin-left: 5%;
      margin-right: 5%;
    }
  }

@media (min-width: 1200px) {
    .main {
      margin-left: 10%;
      margin-right: 10%;
    }
  }
</style>