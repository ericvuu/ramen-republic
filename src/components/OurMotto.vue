<script setup>

</script>

<template>
  <section class="our-motto-container container-fluid">
    <div class="our-motto-content container row">
      <h2>Made In Los Angeles</h2>
      <h3>Savor the authentic Japanese flavors with a touch of LA attitude!</h3>
      <p>Experience the authentic taste of Japan in the heart of Los Angeles. Our modern ramen shop offers a delicious fusion of traditional and contemporary flavors, carefully crafted with fresh, locally sourced ingredients. From our savory broth to our perfectly cooked noodles, every bite is a celebration of the art of ramen. Join us for a satisfying and unforgettable culinary journey.</p>
    </div>

  </section>
</template>

<script>
export default {
  name: 'our-motto',
  props: {},
  components: {}
}
</script>

<style scoped>
.our-motto-container {
  display: flex;
  background-color: var(--pink);
}

.our-motto-content {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  padding: 10vh 0px;
  text-align: center;
}

h2 {
  color: var(--red);
  font-size: 1.2rem;
}

h3 {
  color: var(--red);
  font-size: var(--h3);
  margin-top: 15px;
  -webkit-text-fill-color: var(--pink) !important;
  -webkit-text-stroke: 2px var(--red) !important;
}

p {
  margin-top: 25px;
  font-size: var(--p);
}

</style>
