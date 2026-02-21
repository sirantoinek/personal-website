<script setup lang="ts">
  import { ref, onMounted } from "vue";

  const activeItem = ref("about");
  const navbarItems = ["about", "experience", "projects", "contact"];
  
  let isClickScroll = false; // while true, locks activeItem from updating

  const toggleItemColor = (itemName: string) => {
    activeItem.value = itemName;
    
    isClickScroll = true;
    setTimeout(() => { // after 250ms, set flag back to false
      isClickScroll = false;
    }, 250);
  };

  onMounted(() => {
    const lastId = navbarItems[navbarItems.length - 1];
    const secondToLastId = navbarItems[navbarItems.length - 2];
    if (!lastId || !secondToLastId) return;

    const observerOptions = {
      root: null,
      rootMargin: "-15% 0px -80% 0px",
      threshold: 0
    };

    const observer = new IntersectionObserver((entries) => {
      if (isClickScroll) return; // if flag is true, do not update activeItem

      entries.forEach((entry) => {
        if (entry.isIntersecting && activeItem.value !== lastId) { // does not override lastId if it is currently the active item
          activeItem.value = entry.target.id;
        }
      });
    }, observerOptions);
    
    const lastElement = document.getElementById(lastId);
    if (lastElement) {
      const bottomObserver = new IntersectionObserver((entries) => { // handles last element which may not reach the observed area
        if (isClickScroll) return; // if flag is true, do not update activeItem

        if (entries[0]?.isIntersecting) {
          activeItem.value = lastId;
        } 
        else {
          activeItem.value = secondToLastId;
        }
      }, { threshold: 0.3 }); // activate when entry is at least 30% visible

      bottomObserver.observe(lastElement);
    }

    navbarItems.forEach((id) => {
      const item = document.getElementById(id);
      if (item) observer.observe(item);
    });
  });
</script>

<template>
  <nav class="navbar">
    <div class="navbar__items">
      <router-link 
        v-for="item in navbarItems"
        :key="item"
        class="navbar__item"
        :class="{ active: activeItem === item }"
        @click="toggleItemColor(item)"
        :to="'#' + item"
      >
        {{ item }}
      </router-link>
    </div>
  </nav>
</template>

<style lang="scss">
	.navbar {
    display: flex;
    pointer-events: none;
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
    pointer-events: auto;
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
    text-decoration: none;
    padding: .25rem .5rem;
    border-radius: .25rem;
    transition: background-color 150ms ease-out;
  }

  .navbar__item.active {
    color: inherit;
  }

  .navbar__item:hover {
    background-color: $lm_border;
    transition: background-color 0s;
  }
</style>