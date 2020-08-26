<template>
  <div class="grid grid-cols-3 grid-rows-3 gap-3 md:gap-4 lg:gap-8">
    <GalleryElement
      v-for="(photo, index) in photos"
      :key="index"
      :photo="photo"
    ></GalleryElement>
  </div>
</template>

<script>
import GalleryElement from "@/components/gallery/GalleryElement.vue";
export default {
  components: {
    GalleryElement,
  },
  props: {
    photos: Array,
  },
};
</script>

<style></style>
