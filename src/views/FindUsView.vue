<script setup>
import Footer from '../components/Footer.vue';
</script>

<template>
  <main>
    <h1>This is the Find Us page</h1>
    <Footer />
  </main>
</template>


<script>
export default {
  name: "FindUsView",
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
