<script setup lang="ts">

</script>

<template>
  <div class="aboutMe">
    <h1 class="title-text">Hi, I'm Kevin Sirantoine</h1>
    <p class="body-text">A software developer and computer enthusiast passionate about building practical and efficient applications. 
      <br>I enjoy exploring new technologies, solving problems, and finding creative solutions. When I'm not coding, I'm usually tinkering with computers or enjoying the outdoors.</p>
    <p class="body-text">Lorem ipsum dolor sit amet consectetur adipisicing elit. Sint tempora rerum nesciunt nostrum dolores sed dolorem quae nulla accusantium, eos deleniti, sapiente consectetur ut quisquam illum molestiae? Distinctio, quae blanditiis.</p>
  </div>
</template>

<style lang="scss">
  .aboutMe {
    display: flex;
    flex-direction: column;
    justify-content: flex-start;
		position: relative;
    gap: 1rem;
	}

  .title-text {
    font-size: clamp(3rem, 6vw, 6rem);
    margin-top: 2.5rem;
    margin-bottom: 0px;
    line-height: 1;
  }

  .body-text {
    font-size: 18px;
    margin-bottom: .5rem;
  }
</style>