<script setup>
import { RouterLink } from 'vue-router';
</script>

<template>
  <section class="contact">
    <div class="contact-text-wrapper">
      <div class="logo">
        <RouterLink class="company-logo" to="/">
          <img src="/assets/images/ramen-alt.svg" alt="">
        </RouterLink>
      </div>

      <h3>562.123.4567</h3>
      <ul class="food-apps">
        <li><a href="">Yelp</a></li>
        <li><a href="">Uber Eats</a></li>
        <li><a href="">DoorDash</a></li>
        <li><a href="">Postmates</a></li>
      </ul>
    </div>
  </section>
</template>

<style scoped>
.contact {
  width: 100%;
  color: var(--tan);
  background-color: var(--red);
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  gap: 4rem;
  padding: 10vh 0;
}

.logo {
  display: flex;
  justify-content: center;
}

.company-logo {
  display: flex;
  flex-direction: column;
  align-items: center;
  color: var(--light-tan);
  font-size: var(--h4);
}

.company-logo img {
  width: 100%; /* Make the logo responsive */
  max-width: 300px; /* Limit maximum width for larger screens */
}

h3 {
  font-size: var(--h3);
  text-align: center;
  color: var(--light-tan);
}

.food-apps {
  margin-top: 2rem;
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
  list-style-type: none;
  padding: 0;
}

.food-apps li {
  margin: 0.5rem;
}

.food-apps a {
  color: var(--light-tan);
  font-size: var(--h4);
  border-bottom: 2px dashed var(--light-tan);
  transition: border-bottom 0.2s ease-in-out;
}

.food-apps a:hover {
  border-bottom: 2px solid var(--light-tan);
}
</style>
