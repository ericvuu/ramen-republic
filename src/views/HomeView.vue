<script setup>
  import CallToAction from '../components/CallToAction.vue';
  import Hero from '../components/Hero.vue';
  import OurMotto from '../components/OurMotto.vue';
  import ChefSpecial from '../components/ChefSpecial.vue';
  import AboutUs from '../components/AboutUs.vue';
  import Hours from '../components/Hours.vue';
  import Contact from '../components/Contact.vue';
</script>

<template>
  <main>
    <Hero />
    <CallToAction />
    <OurMotto />
    <ChefSpecial />
    <AboutUs />
    <Hours />
    <Contact />
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
    AboutUs,
    Hours,
    Contact
  },
  data() {
    return {};
  },
  methods: {},
};


</script>
