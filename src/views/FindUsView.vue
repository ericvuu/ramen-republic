<script setup>
import Contact from '../components/Contact.vue';
import 'leaflet/dist/leaflet.css';
import L from 'leaflet';
import { ref, onMounted } from 'vue';

const mapContainer = ref(null);

onMounted(() => {

  const map = L.map(mapContainer.value).setView([51.505, -0.09], 13);

  L.tileLayer('https://{s}.tile.openstreetmap.org/{z}/{x}/{y}.png', {}).addTo(map);

  L.marker([34.0522, -118.2437]).addTo(map)
    .bindPopup('Los Angeles, CA')
    .openPopup();
});
</script>

<template>
  <main>
    <h1>Find Us</h1>
    <div ref="mapContainer" class="map-container"></div>
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
.map-container {
  height: 400px;
  width: 100%;
  border: 2px solid #ddd;
  border-radius: 8px;
  margin: 0 auto;

  @media (min-width: 1024px) {
    height: 600px;
    width: 60%;
    margin: 3rem auto;
  }
}
</style>

<script>
export default {
  name: "FindUsView",
  props: {},
  components: {
    Contact
  },
  data() {
    return {};
  },
  methods: {},
};


</script>
