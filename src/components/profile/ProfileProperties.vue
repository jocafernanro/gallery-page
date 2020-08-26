<template>
  <div class="bg-gray-300 rounded-xl text-center p-3 sm:p-4 leading-3">
    <span class="block sm:text-sm text-xxs sm:mb-2">{{ property.data }}</span>
    <span class="sm:text-sm text-xxs">{{ property.name }}</span>
  </div>
</template>

<script>
export default {
  props: {
    property: Object,
  },
};
</script>

<style></style>
