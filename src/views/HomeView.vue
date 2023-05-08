<script setup>
  import CallToAction from '../components/CallToAction.vue';
  import Hero from '../components/Hero.vue';
  import OurMotto from '../components/OurMotto.vue';
  import ChefSpecial from '../components/ChefSpecial.vue';
  import AboutUs from '../components/AboutUs.vue';
</script>

<template>
  <main>
    <Hero />
    <CallToAction />
    <OurMotto />
    <ChefSpecial />
    <AboutUs />
  </main>
</template>


<script>
export default {
  name: "HomeView",
  props: {},
  components: {
    CallToAction,
    Hero,
    OurMotto,
    ChefSpecial,
    AboutUs
  },
  data() {
    return {};
  },
  methods: {},
};


</script>
