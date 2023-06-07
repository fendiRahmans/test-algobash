<template>
  <div>
    <header-menu />
    <Nuxt />
  </div>
</template>

<script>
import HeaderMenu from "~/components/header-menu.vue";
export default {
  components: { HeaderMenu },
  head() {
    return {
      script: [
        {
          src: "https://kit.fontawesome.com/7104542cb7.js",
        },
        {
          crossorigin: "anonymous",
        },
      ],
    };
  },
};
</script>

<style>
</style>