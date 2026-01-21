<script setup lang="ts">
  import profileImage1 from '../assets/profile_photo1.png';
  import profileImage2 from '../assets/profile_photo2.png';
</script>

<template>
  <div class="aboutMe">
    <h1 class="title-text">
      <span>Hi I'm</span>
      <span>Kevin Sirantoine</span>
    </h1>
    <span class="desc">
      <p class="desc-text">A software developer and computer enthusiast passionate about building practical and efficient applications. 
        <br>I enjoy exploring new technologies, solving problems, and finding creative solutions. 
        <br>When I'm not coding, I'm usually tinkering with computers or enjoying the outdoors.
      </p>
      <div class="photo-frame">
        <div class="photos">
          <img :src="profileImage1" alt="profile image 1" class="photo"/>
          <img :src="profileImage2" alt="profile image 2" class="photo"/>
        </div>
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
    gap: 1rem;
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

  .photo-frame {
    width: 100%;
    max-width: 200px;
    border-radius: .5rem;
    height: auto;
    overflow: hidden;
    flex-grow: 2;
    transition: 150ms;
  }

  .photos {
    display: flex;
    width: 200%;
    border-radius: .5rem;
    height: auto;
    flex-grow: 2;
    transition: 150ms;
    animation: switchPhotos 12.5s infinite ease;
  }

  .photo {
    width: 100%;
    border-radius: .5rem;
    height: auto;
    flex-grow: 2;
    transition: 150ms;
  }

  .photo-frame:hover {
    transform: scale(1.05);
  }

  .desc {
    display: flex;
    flex-direction: column;
    flex-wrap: wrap;
    gap: 1rem;
  }

  .desc-text {
    font-size: 18px;
    margin-bottom: .5rem;
    text-wrap-style: pretty;
  }

  @media (min-width: 900px) and (max-width: 1464px) {
    .desc {
      flex-direction: row;
      flex-wrap: nowrap;
    }

    .profile-image {
      width: 50%;
    }

    .desc-text {
      width: 50%;
    }
  }

  @keyframes switchPhotos {
  0%, 41% { transform: translateX(0); }
  45% { transform: translateX(-50%); }
  45%, 81% { transform: translateX(-50%); }
  85% { transform: translateX(0); }
  85%, 100% { transform: translateX(0); }
  }
</style>