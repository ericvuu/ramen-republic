<script setup>
import { RouterLink } from 'vue-router';
</script>

<template>
  <section class="footer">
    <div class="footer-text-wrapper">
        <div class="logo">
          <RouterLink class="company-logo" to="/"><img src="/assets/images/ramen-alt.svg" alt=""></RouterLink>
        </div>

      <h1>562.123.4567</h1>
      <ul class="food-apps">
        <li><a href="">Yelp</a></li>
        <li><a href="">Uber Eats</a></li>
        <li><a href="">DoorDash</a></li>
        <li><a href="">Postmates</a></li>
      </ul>
    </div>
  </section>
</template>

<script>
export default {
  name: 'footer',
  props: {},
  components: {}
}
</script>

<style scoped>
.footer {
  width: 100%;
  color: var(--tan);
  background-color: var(--red);
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  gap: 4rem;
  padding: 10vh 0px;
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
  width: 300px;
}

h1 {
  font-size: var(--h1);
  text-align: center;
  color: var(--light-tan);
}

.food-apps {
  margin-top: 2rem;
  display: flex;
  flex-direction: row;
  justify-content: space-evenly;
  list-style-type: none;
  padding: 0;
}

li:not(:last-child) {
  margin-right: 3rem;
}

.food-apps a {
  color: var(--light-tan);
  font-size: var(--h4);
  border-bottom: 2px dashed var(--light-tan);
}

.food-apps a:hover {
  border-bottom: 2px solid var(--light-tan);
}

h4 {
  font-size: var(--h4);
  text-align: center;
}

p {
  font-size: var(--p-large);
  text-align: center;
  padding: 1rem;
  color: black;
}
</style>
