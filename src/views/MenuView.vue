<script setup>
import ChefSpecial from '../components/ChefSpecial.vue';
import StandardMenu from '../components/StandardMenu.vue';
import Footer from '../components/Footer.vue';

</script>

<template>
  <main>
    <ChefSpecial />
    <StandardMenu/>
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
  name: "MenuView",
  props: {},
  components: {
    StandardMenu,
    ChefSpecial,
    Footer
  },
  data() {
    return {};
  },
  methods: {},
};


</script>
