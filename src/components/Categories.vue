<template>
  <section id="categories" class="py-16 scroll-mt-20 bg-white">
    <div class="container mx-auto px-4">
      <!-- Section Header -->
      <div class="text-center mb-12">
        <h2 class="text-3xl font-bold text-amber-950 mb-3">
          Explore Our Fragrance Collections
        </h2>
        <p class="text-lg text-gray-800 max-w-2xl mx-auto">
          Discover scents that match your personality
        </p>
      </div>

      <!-- Categories Grid -->
      <div class="grid grid-cols-1 sm:grid-cols-3 gap-6">
        <div
          v-for="(category, index) in categories"
          :key="index"
          class="relative group overflow-hidden rounded-lg transition-shadow duration-300"
        >
          <div class="h-64" overflow-hidden>
            <img
              :src="category.image"
              :alt="category.alt"
              class="w-full h-full object-cover group-hover:scale-105 transition-transform duration-500"
            />
          </div>
          <div
            class="absolute inset-0 bg-gradient-to from-black/60 via-transparent to-transparent"
          >
            <div class="absolute bottom-0 left-0 p-6">
              <h3 class="text-xl font-semibold text-amber-950">
                {{ category.title }}
              </h3>
              <p class="text-amber-950 mt-1">{{ category.description }}</p>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>
<script setup>
import { ref } from "vue";
import Per1 from "../assets/Per1.png";
import Per2 from "../assets/Per2.png";
import Per3 from "../assets/Per3.png";
import Per4 from "../assets/Per4.png";
import Per5 from "../assets/Per5.png";
import Per6 from "../assets/Per6.png";

const categories = ref([
  {
    image: Per1,
    title: "Men's Collection",
    description: "Imperial Majesty",
    alt: "Men's Collection",
  },
  {
    image: Per2,
    title: "Women's Collection",
    description: "Amouage Tribute Attar",
    alt: "Women's Collection",
  },
  {
    image: Per3,
    title: "Men's Collection",
    description: "Tom Ford",
    alt: "Men's Collection",
  },
  {
    image: Per4,
    title: "Men's Collection",
    description: "Royal Oud",
    alt: "Men's Collection",
  },
  {
    image: Per5,
    title: "Men's Collection",
    description: "The Moon",
    alt: "Men's Collection",
  },
  {
    image: Per6,
    title: "Women's Collection",
    description: "Flowerbomb",
    alt: "Men's Collection",
  },
]);
</script>
