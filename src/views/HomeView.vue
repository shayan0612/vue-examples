<script setup>
import Hero from "../components/Hero.vue";
import HomeCards from "../components/HomeCards.vue";
import CardsListing from "../components/CardsListings.vue";
</script>

<template>
  <Hero />
  <HomeCards />
  <CardsListing :limit="3" :showBtn="true" />
</template>
