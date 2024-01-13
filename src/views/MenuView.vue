<script setup>
import ChefSpecial from '../components/ChefSpecial.vue';
import StandardMenu from '../components/StandardMenu.vue';
import Contact from '../components/Contact.vue';

</script>

<template>
  <main>
    <ChefSpecial />
    <StandardMenu/>
    <Contact />
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
    Contact
  },
  data() {
    return {};
  },
  methods: {},
};


</script>
