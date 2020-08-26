<template>
  <header class="flex flex-col items-center my-12">
    <img
      src="images/profilePhoto.png"
      class="rounded-xxl sm:w-32 w-24 m-3"
      alt="Profile picture"
    />
    <h1 class="md:text-xl text-md">{{ profile.name }}</h1>
    <h2 class="text-gray-400 text-xs md:m-1 text-md">{{ profile.location }}</h2>
    <div class="grid grid-cols-3 m-3 gap-2">
      <ProfileProperties
        v-for="(property, index) in profile.properties"
        :key="index"
        :property="property"
      ></ProfileProperties>
    </div>
  </header>
</template>

<script>
import ProfileProperties from "@/components/profile/ProfileProperties.vue";

export default {
  components: {
    ProfileProperties,
  },
  props: {
    profile: Object,
  },
};
</script>

<style></style>
