<script setup>
import Footer from '../components/Footer.vue';
</script>


<template>
  <div class="menu">
    <h1>This is the Menu page</h1>
    <Footer />
  </div>
</template>

<style>

</style>


<script>
export default {
  name: "MenuView",
  props: {},
  components: {
    Footer
  },
  data() {
    return {};
  },
  methods: {},
};


</script>
