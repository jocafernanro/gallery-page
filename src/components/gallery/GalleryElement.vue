<template>
  <img
    :src="photo.url"
    class="rounded-xl shadow-lg w-full min-w-full"
    :class="`row-span-${photo.rowSpan} col-span-${photo.colSpan}`"
    alt=""
  />
</template>

<script>
export default {
  props: {
    photo: Object,
  },
};
</script>

<style></style>
