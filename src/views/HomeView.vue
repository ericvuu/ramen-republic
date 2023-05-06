<script setup>
  import CallToAction from '../components/CallToAction.vue';
  import Hero from '../components/Hero.vue';
  import OurMotto from '../components/OurMotto.vue';
</script>

<template>
  <main>
    <Hero />
    <CallToAction />
    <OurMotto />
  </main>
</template>


<script>
export default {
  name: "HomeView",
  props: {},
  components: {
    CallToAction,
    Hero,
    OurMotto
  },
  data() {
    return {};
  },
  methods: {},
};


</script>
