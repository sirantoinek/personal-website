<script setup lang="ts">
  import { ref } from "vue";

  const activeItem = ref("about");
  const navbarItems = ["about", "experience", "projects", "contact"];

  const toggleColor = (itemName: string) => {
    activeItem.value = itemName;
  };
</script>

<template>
  <nav class="navbar">
    <div class="navbar__items">
      <a 
        v-for="item in navbarItems"
        :key="item"
        class="navbar__item"
        :class="{ active: activeItem === item }"
        @click="toggleColor(item)"
      >
        {{ item }}
      </a>
    </div>
  </nav>
</template>

<style lang="scss">
	.navbar {
    display: flex;
    justify-content: left;
		position: sticky;
    z-index: 1;
  	top: 20px;
    left: 20px;
	}

  @media (max-width: 600px) {
    .navbar {
      justify-content: center;
    }
  }

  .navbar__items {
    display: flex;
    padding: .25rem;
    background-color: $lm_background;
    backdrop-filter: blur(5px);
    border: 1px solid $lm_border;
    border-radius: .5rem;
    box-shadow: rgba(0, 0, 0, 0.1) 0px 1px 3px 0px, rgba(0, 0, 0, 0.06) 0px 1px 2px 0px;
    font-size: 1rem;    
  }

  .navbar__item {
    color: $lm_dim;
    padding: .25rem .5rem;
    border-radius: .25rem;
    transition: background-color 150ms ease-out;
  }

  .navbar__item.active {
    color: revert;
  }

  .navbar__item:hover {
    background-color: $lm_border;
    transition: background-color 0s;
  }

</style>