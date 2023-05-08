<script setup></script>

<template>
  <section class="chef-special-container container-fluid">
    <div class="chef-special-content container row">
      <h2>Chef's Daily Specials</h2>

      <div class="special-items">
        <div class="special-item" v-for="(special, index) in specials" v-bind:key="index">
          <h3 class="category">{{ special.category }}</h3>
          <p class="name">{{ special.name }}</p>
          <p class="description">{{ special.description }}</p>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export async function getAllSpecials() {
  const response = await fetch('specials.json')
  return await response.json()
}

export default {
  name: 'chef-special',
  props: {},
  data() {
    return {
      specials: []
    }
  },
  methods: {
    getAllSpecials() {
      getAllSpecials().then((response) => {
        this.specials = response
      })
    }
  },
  created() {
    this.getAllSpecials()
  },
  components: {}
}
</script>

<style scoped>
.chef-special-container {
  display: flex;
  background-color: var(--tan);
}

.chef-special-content {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  padding: 5vh 0px;
  text-align: center;
}

.special-items {
  display: flex;
  justify-content: space-between;
  margin-top: 40px;
}

.special-item {
  width: 45%;
  text-align: center;
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
</style>
