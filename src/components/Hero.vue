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

<script>
export default {
  name: 'Hero',
  props: {},
  components: {}
}
</script>

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
}

p {
   color: var(--red);
  font-size: 2rem;
  font-weight: 800;
}


.hero .wrapper {
  min-height: 80vh;
  background-size: cover;
  background-position: center center;
  background-color: var(--tan);
  display: flex;
  flex-direction: column;
  -webkit-box-pack: center;
  justify-content: center;
  align-items: center;
}
</style>
