<script setup></script>

<template>
  <section class="hero">
    <div
      class="wrapper container"
      v-bind:style="{ backgroundImage: 'url(assets/images/hero-image.jpg)' }"
    >
      <h1>We are Ramen Republic</h1>
      <p>Authentic Japanese flavors with a California twist!</p>
    </div>
  </section>
</template>

<style scoped>
.hero {
  width: 100%;
  min-height: 90vh;
  background-color: var(--tan);
  display: flex;
  justify-content: center;
  align-items: center;
}

h1 {
  color: var(--red);
  font-size: 7rem;
  text-align: center;
}

p {
  color: var(--red);
  font-size: 2rem;
  font-weight: 800;
  text-align: center;
}

.hero .wrapper {
  min-height: 80vh;
  background-size: cover;
  background-position: center center;
  background-color: var(--tan);
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
}

@media (max-width: 768px) {

  h1 {
    font-size: 4rem;
  }

  p {
    font-size: 1.5rem;
  }
}
</style>
