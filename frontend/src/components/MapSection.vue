<script setup>
import { openLightbox } from "../lib/lightbox";
import { LAST_KNOWN_LOCATION } from "../lib/constants";

const MAP_PHOTO = {
  url: "/photos/location-timeline-search-area.jpg",
  caption: "Location timeline and likely search area for Arpan, Bhavin and Karan",
};
</script>

<template>
  <div class="h-full rounded-xl border border-gray-200 bg-white p-5 shadow-sm sm:p-6">
    <p class="text-center text-xs font-semibold uppercase tracking-wide text-gray-500">
      Last Known Location &amp; Nearby Resources
    </p>
    <button
      type="button"
      class="mt-3 block w-full overflow-hidden rounded-lg border border-gray-200"
      @click="openLightbox(MAP_PHOTO.url, MAP_PHOTO.caption)"
    >
      <img
        :src="MAP_PHOTO.url"
        :alt="MAP_PHOTO.caption"
        loading="lazy"
        class="w-full cursor-pointer object-cover"
      />
    </button>
    <p class="mt-2 text-xs text-gray-500">{{ MAP_PHOTO.caption }}</p>
    <p class="mt-1 text-xs text-gray-500">
      Coordinates: {{ LAST_KNOWN_LOCATION.lat.toFixed(4) }}, {{ LAST_KNOWN_LOCATION.lng.toFixed(4) }}
    </p>
  </div>
</template>
