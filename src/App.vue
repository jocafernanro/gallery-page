<template>
  <div id="app" class="container mx-auto p-3">
    <BaseProfile :profile="profile"></BaseProfile>
    <BaseGallery :photos="profile.photos"></BaseGallery>
    <BaseFooter></BaseFooter>
  </div>
</template>

<script>
import BaseProfile from "@/components/BaseProfile.vue";
import BaseGallery from "@/components/BaseGallery.vue";
import BaseFooter from "@/components/BaseFooter.vue";

export default {
  name: "App",
  components: {
    BaseProfile,
    BaseGallery,
    BaseFooter,
  },
  data: function() {
    return {
      profile: {
        name: "Rodney Cotton",
        location: "Helsinki, Finland",
        properties: [
          { name: "Posts", data: 100 },
          { name: "Followers", data: 2242 },
          { name: "Following", data: 1432 },
        ],
        photos: [
          { url: "images/photo1.png", rowSpan: 1, colSpan: 1 },
          { url: "images/photo2.png", rowSpan: 1, colSpan: 2 },
          { url: "images/photo3.png", rowSpan: 1, colSpan: 2 },
          { url: "images/photo4.png", rowSpan: 2, colSpan: 1 },
          { url: "images/photo5.png", rowSpan: 1, colSpan: 1 },
          { url: "images/photo6.png", rowSpan: 1, colSpan: 1 },
        ],
      },
    };
  },
};
</script>

<style>
:root {
  --global-font-family: "Montserrat", "Helvetica Neue", -apple-system,
    BlinkMacSystemFont, "Segoe UI", Roboto, Arial, sans-serif;
  --global-font-size: 1rem;
  --font-weight-regular: 400;
  --font-weight-bold: 700;
}
html,
body {
  font-family: var(--global-font-family);
  font-size: 16px;
  font-weight: var(--font-weight-regular);
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  word-spacing: 1px;
  -ms-text-size-adjust: 100%;
  -webkit-text-size-adjust: 100%;
  -moz-osx-font-smoothing: grayscale;
  -webkit-font-smoothing: antialiased;
  box-sizing: border-box;
  scroll-behavior: smooth;
  max-width: 1920px;
  margin: 0 auto;
}
</style>
