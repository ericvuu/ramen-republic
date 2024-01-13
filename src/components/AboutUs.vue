<script setup></script>

<template>
  <section class="about-us">
    <div class="about-image-wrapper">
      <div class="about-image" />
    </div>
    <div class="about-text-wrapper">
      <div class="container">
        <h2>Chef Yamamoto</h2>
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

<style scoped>
.about-us {
  width: 100%;
  color: var(--red);
  display: flex;
  flex-direction: column;
}

.about-image-wrapper {
  padding: 0 1rem;
  position: relative;
  bottom: -6rem;
}

.about-image {
  width: 100%;
  height: auto;
  max-width: 800px;
  margin: auto;
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
  text-align: center;
}

.section-title {
  font-size: var(--h4);
  padding: 1rem;
}

h2 {
  font-size: var(--h2);
  -webkit-text-fill-color: var(--tan) !important;
  -webkit-text-stroke: 2px var(--red) !important;
}

h4 {
  font-size: var(--h4);
}

p {
  font-size: var(--p-large);
  padding: 1rem;
}

@media (max-width: 768px) {
  .about-text-wrapper {
    padding: 2rem 1rem;
  }

  .about-image-wrapper {
    bottom: 0;
  }
}
</style>
