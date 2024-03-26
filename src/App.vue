<script setup lang="ts">
import Navbar from './components/Navbar.vue'
</script>

<template>
  <div class="background-section">
    <Navbar />
    <div class="hero-container">
      <img class="audio-wave" src="/audio.gif" />
      <img id="hero-image" src="/felek-icon.svg" />
      <img class="audio-wave second" src="/audio.gif" />
    </div>
    <div class="social-bar-container">
     <div class="social-header">
      <h2>Join Us</h2>
     </div>
    </div>

  </div>


</template>

<style scoped>

h2 {
  color: white;
  font-family: 'Lemon Milk';
}
.hero-container {
  display: flex;
  justify-content: space-evenly;
  height: 80vh;
  align-items: center;
}

.social-bar-container {
  height: 20vh;
  display: flex;
  justify-content: center;
}

.audio-wave {
  width: 400px;
  height: 400px;
  object-fit: cover;
  object-position: 25% 25%;
}

.second {
  transform: scaleX(-1);
}

#hero-image {
  height: 60vh;
  display: block;
  filter: grayscale(100%);
  mix-blend-mode: difference;
}

.background-section {
  position: fixed;
  background-image: url('./assets/background.jpg');
  background-size: cover;
  background-position: top;
  background-repeat: no-repeat;
  width: 100%;
  height: 100vh;
}
</style>
