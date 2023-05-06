<script setup>
  import CallToAction from '../components/CallToAction.vue';
  import Hero from '../components/Hero.vue';
</script>

<template>
  <main>
    <Hero />
    <CallToAction />
  </main>
</template>


<script>
export default {
  name: "HomeView",
  props: {},
  components: {
    CallToAction
  },
  data() {
    return {};
  },
  methods: {},
};


</script>
