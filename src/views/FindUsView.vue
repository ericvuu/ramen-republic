<script setup>
import Footer from '../components/Footer.vue';
import 'leaflet/dist/leaflet.css'; // Import Leaflet CSS
import L from 'leaflet';
import { ref, onMounted } from 'vue';

const mapContainer = ref(null);

onMounted(() => {
  // Initialize the map
  const map = L.map(mapContainer.value).setView([51.505, -0.09], 13);

  // Add a tile layer (you can use your preferred tile layer)
  L.tileLayer('https://{s}.tile.openstreetmap.org/{z}/{x}/{y}.png', {}).addTo(map);

  // Add a marker
  L.marker([34.0522, -118.2437]).addTo(map)
    .bindPopup('Los Angeles, CA')
    .openPopup();
});
</script>

<template>
  <main>
    <h1>Find Us</h1>
    <div ref="mapContainer" class="map-container"></div>
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
    Footer
  },
  data() {
    return {};
  },
  methods: {},
};


</script>
