<template>
  <section class="standard-menu-container container-fluid">
    <div class="standard-menu-content container row">
      <h2>Main Menu</h2>

      <div class="standard-items" v-if="items.length > 0">
        <template v-for="(item, index) in items" :key="index">
          <!-- Display category name only if it's the first item in the category -->
          <template v-if="index === 0 || items[index - 1].category !== item.category">
            <h3 class="category">{{ item.category }}</h3>
          </template>

          <div class="standard-item">
            <p class="name">{{ item.name }}</p>
            <p class="description">{{ item.description }}</p>
          </div>
        </template>
      </div>

      <div v-else>
        <!-- Add a message or loading indicator for when items are undefined or empty -->
        <p>Loading...</p>
      </div>
    </div>
  </section>
</template>

<script>
export async function getAllItems() {
  const response = await fetch('menu.json');
  return await response.json();
}

export default {
  name: 'standard-menu',
  props: {},
  data() {
    return {
      items: []
    };
  },
  methods: {
    async getAllItems() {
      try {
        const response = await fetch('menu.json');
        this.items = await response.json();
      } catch (error) {
        console.error('Error fetching items:', error);
      }
    }
  },
  created() {
    this.getAllItems();
  },
  components: {}
};
</script>

<style scoped>
.standard-menu-container {
  display: flex;
  background-color: var(--tan);
}

.standard-menu-content {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  padding: 10vh 0px;
  text-align: center;
}

.standard-items {
  display: flex;
  flex-direction: column; /* Change to column */
  align-items: center; /* Align items to center */
  margin-top: 40px;
}

.standard-item {
  width: 100%; /* Full width of the container */
  text-align: center;
  margin-top: 20px; /* Add margin for spacing between items */
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
  margin-top: 15px; /* Adjust spacing */
  color: black;
}

.category {
  margin-top: 3rem;
}
</style>
