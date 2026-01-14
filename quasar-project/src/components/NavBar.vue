<template>
  <nav class="navbar">
    <div class="navbar__items">
      <a class="navbar__item">about</a>
      <a class="navbar__item">experience</a>
      <a class="navbar__item">projects</a>
      <a class="navbar__item">contact</a>
    </div>
  </nav>
</template>

<style>
	.navbar {
    display: flex;
    justify-content: left;
		position: sticky;
  	top: 20px;
    left: 20px;
	}

  @media (max-width: 600px) {
    .navbar {
      justify-content: center;
    }
  }

  .navbar__items {
    padding: .25rem;
    border: 1px solid #e5e5e5;
    border-radius: .5rem;
    box-shadow: rgba(0, 0, 0, 0.1) 0px 1px 3px 0px, rgba(0, 0, 0, 0.06) 0px 1px 2px 0px;
    font-size: 1rem;
  }

  .navbar__item {
    padding: .25rem .5rem;
  }
</style>