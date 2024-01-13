<script setup>
import { ref, onMounted } from 'vue';

const specials = ref([]);

const getAllSpecials = async () => {
  try {
    const response = await fetch('specials.json');
    specials.value = await response.json();
  } catch (error) {
    console.error('Error fetching specials:', error);
  }
};

onMounted(() => {
  getAllSpecials();
});
</script>

<template>
  <section class="chef-special-container container-fluid">
    <div class="chef-special-content container row">
      <h2>Chef's Daily Specials</h2>

      <div class="special-items">
        <div class="special-item" v-for="(special, index) in specials" :key="index">
          <h3 class="category">{{ special.category }}</h3>
          <p class="name">{{ special.name }}</p>
          <p class="description">{{ special.description }}</p>
        </div>
      </div>
    </div>
  </section>
</template>

<style scoped>
.chef-special-container {
  background-color: var(--tan);
}

.chef-special-content {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  padding: 10vh 0 2vh 0;
  text-align: center;
}

.special-items {
  display: flex;
  flex-wrap: wrap;
  justify-content: space-around;
  margin-top: 40px;
}

.special-item {
  width: 45%;
  margin-bottom: 20px;
  text-align: center;
  padding: 20px;
}

h2 {
  color: var(--red);
  font-size: var(--h2);
}

h3 {
  color: var(--red);
  font-size: var(--h3);
  margin-top: 15px;
}

p {
  margin-top: 15px;
}

.name {
  font-size: var(--p-large);
  margin-top: 25px;
  color: var(--red);
  text-transform: uppercase;
  font-weight: 500;
}

.description {
  font-size: var(--p);
  margin-top: 25px;
  color: black;
}

@media (max-width: 768px) {
  .special-item {
    width: 100%;
  }
}
</style>
