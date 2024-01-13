<script setup></script>

<template>
  <section
    class="menu-header"
    v-bind:style="{ backgroundImage: 'url(assets/images/ramen-menu-header.jpg)' }"
  >
    <h1>Discover Our Menu</h1>
  </section>
</template>

<script>
export default {
  name: 'menu-header',
  props: {},
  components: {}
}
</script>

<style scoped>
.menu-header {
  width: 100%;
  min-height: 30vh;
  background-size: cover;
  background-position: center center;
  display: flex;
  justify-content: center;
  align-items: center;
  background-color: var(--tan);
}

h1 {
  color: var(--red);
  font-size: 4rem;
}

p {
  color: var(--red);
  font-size: 2rem;
  font-weight: 800;
}
</style>
