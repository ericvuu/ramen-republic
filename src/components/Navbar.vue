<script setup>
import { RouterLink } from 'vue-router';
</script>

<template>
  <nav>
    <div class="container-fluid">
      <div class="container row space-between">
        <div class="logo">
          <RouterLink class="company-logo" to="/"><img src="/assets/images/ramen.svg" alt="">Ramen Republic</RouterLink>
        </div>
        <div class="nav-links">
          <div class="nav-link">
            <RouterLink to="/menu">Menu</RouterLink>
          </div>
          <div class="nav-link">
            <RouterLink to="/find-us">Find Us</RouterLink>
          </div>
        </div>
      </div>
    </div>
  </nav>
</template>

<script>
export default {
  name: 'Navbar',
  props: {},
  components: {}
}
</script>

<style scoped>
nav {
  width: 100%;
  background-color: var(--light-tan);
  padding: 1.5rem 1rem;
}

.company-logo {
  display: flex;
  align-items: center;
}
.company-logo img {
  max-width: 80px;
}

.nav-links {
  display: flex;
  align-items: center;
}

.nav-link:first-child {
  margin-right: 15px;
}
</style>
