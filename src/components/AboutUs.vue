<script setup></script>

<template>
  <section class="about-us">
    <div class="about-image-wrapper">
      <div class="about-image" src="" />
    </div>
    <div class="about-text-wrapper">
      <div class="container">
        <h1>Chef Yamamoto</h1>
        <h4 class="section-title">Our story</h4>
        <div class="section-description">
          <p>
            Yamamoto is an incredibly talented chef with a passion for creating mouth-watering ramen
            dishes that leave his customers craving more. He has spent his entire career perfecting
            the art of ramen-making, starting with his apprenticeship in Tokyo's bustling restaurant
            scene and continuing through his time as the head chef at several renowned ramen
            restaurants.
          </p>
          <p>
            At Ramen Republic, Yamamoto brings his expertise and passion to every bowl of ramen he
            serves. Whether you're in the mood for classic Shoyu or adventurous Tsukemen, Yamamoto's
            creative twists on traditional recipes will leave you fully satisfied and eager to
            return. His commitment to excellence is reflected not only in the quality of his dishes
            but also in the welcoming atmosphere he cultivates within his restaurant. From the
            attentive service to the cozy decor, Yamamoto's attention to detail is evident in every
            aspect of the dining experience.
          </p>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: 'about-us',
  props: {},
  components: {}
}
</script>

<style scoped>
.about-us {
  width: 100%;
  color: var(--red);
  display: flex;
  flex-direction: column;
  justify-content: flex-start;
  gap: 4rem;
}

.about-image-wrapper {
  padding: 0 1rem;
  z-index: 2;
  position: relative;
  bottom: -6rem;
}

.about-image {
  width: 70%;
  margin: auto;
  height: 35vw;
  background-size: cover;
  background-position: center right;
  background-color: var(--red);
  background-image: url('assets/images/about-us.jpg');
}

.about-text-wrapper {
  padding: 4rem 1rem;
  background-color: var(--tan);
  display: flex;
  flex-direction: column;
  gap: 2rem;
}

.section-title {
  font-size: var(--h4);
  text-align: center;
  padding: 1rem;
}

h1 {
  font-size: var(--h1);
  text-align: center;
  -webkit-text-fill-color: var(--tan) !important;
  -webkit-text-stroke: 2px var(--red) !important;
}

h4 {
  font-size: var(--h4);
}

p {
  font-size: var(--p-large);
  text-align: center;
  padding: 1rem;
}
</style>
