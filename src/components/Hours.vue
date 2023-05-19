<script setup></script>

<template>
  <section class="hours">
    <div class="hours-text-wrapper">
      <h1>Opening Hours</h1>
      <div class="time-block">
        <h4>Happy Hour</h4>
        <p>3:30 PM - 5:30 PM</p>
      </div>
      <div class="time-block">
        <h4>Monday - Friday</h4>
        <p>10:00 AM - 10:00 PM</p>
      </div>
      <div class="time-block">
        <h4>Saturday</h4>
        <p>10:00 AM - 12:00 PM</p>
      </div>
      <div class="time-block">
        <h4>Sunday</h4>
        <p>10:00 AM - 8:00 PM</p>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: 'hours',
  props: {},
  components: {}
}
</script>

<style scoped>
.hours {
  width: 100%;
  color: var(--red);
  background-color: var(--pink);
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  gap: 4rem;
  padding: 10vh 0px;
}

h1 {
  font-size: var(--h1);
  text-align: center;
  color: var(--red);
}

.time-block {
  margin-top: 2rem;
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
