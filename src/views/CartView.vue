<script setup>

import Footer from '../components/Footer.vue';

</script>

<template>
  <main>
    <h1>Cart</h1>
    <Footer />
  </main>
</template>

<style scoped>
h1 {
  color: var(--red);
  font-size: 5.2rem;
  text-align: center;
  margin-top: 3rem;
}
</style>

<script>
export default {
  name: "CartView",
  props: {},
  components: {
    Footer
  },
  data() {
    return {
      items: [],
      specials: []
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
    },
    async getAllSpecials() {
      try {
        const response = await fetch('specials.json');
        this.specials = await response.json();
      } catch (error) {
        console.error('Error fetching specials:', error);
      }
    },
  },
  created() {
    this.getAllItems();
  },
};


</script>
