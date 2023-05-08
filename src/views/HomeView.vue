<script setup>
  import CallToAction from '../components/CallToAction.vue';
  import Hero from '../components/Hero.vue';
  import OurMotto from '../components/OurMotto.vue';
  import ChefSpecial from '../components/ChefSpecial.vue';
</script>

<template>
  <main>
    <Hero />
    <CallToAction />
    <OurMotto />
    <ChefSpecial />
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
    ChefSpecial
  },
  data() {
    return {};
  },
  methods: {},
};


</script>
