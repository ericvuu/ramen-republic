<script setup>
import { RouterLink } from 'vue-router'
</script>

<template>
  <section class="call-to-action-container container-fluid">
    <RouterLink
      to="/find-us"
      class="call-to-action-image call-to-action-image-1"
      v-bind:style="{ backgroundImage: 'url(assets/images/call-to-action-find-us.jpg)' }"
    >
      <div class="call-to-action-button" v-bind:style="{ backgroundImage: 'url(assets/images/blob.svg)' }">
        Find Us
      </div>
    </RouterLink>
    <RouterLink
      to="/find-us"
      class="call-to-action-image call-to-action-image-2"
      v-bind:style="{ backgroundImage: 'url(assets/images/call-to-action-menu.jpg)' }"
    >
      <div class="call-to-action-button" v-bind:style="{ backgroundImage: 'url(assets/images/blob.svg)' }">
        Our Menu
      </div>
    </RouterLink>
  </section>
</template>

<script>
export default {
  name: 'call-to-action',
  props: {},
  components: {}
}
</script>

<style scoped>
.call-to-action-container {
  display: flex;
}

.call-to-action-image {
  width: 50%;
  min-height: 50vh;
  background-size: cover;
  background-position: center center;
  background-color: var(--red);
  display: flex;
  flex-direction: column;
  -webkit-box-pack: center;
  justify-content: center;
  align-items: center;
}

.call-to-action-button {
  background-repeat: no-repeat;
  background-position: center;
  background-size: contain;
  padding: 4rem;
  font-size: var(--h1);
  opacity: 1;
  transition: opacity 0.2s ease-in-out 0s;
}

.call-to-action-button:hover {
    background-size: contain;
    background-image: url("assets/images/blob-hover.svg") !important;
}
</style>
