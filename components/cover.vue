<template>
  <div class="hero-background">
    <div class="hero-background-top"></div>
    <b-img
      :src="require('~/assets/images/background-cover.png')"
      style="width: 100%; margin-top: -80px; height: 420px"
    >
    </b-img>
    <div class="text-bottom">
      <p class="text-title text-white">Discover Your Wonder</p>
      <p class="text-content text-white">
        Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod
        tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim
        veniam.
      </p>
    </div>
    <div
      class="shadow-sm button-scroll d-flex justify-content-center align-items-center"
    >
      <a href="#who-we-are">
        <i class="fa fa-arrow-down" style="font-size: 20px"></i>
      </a>
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style>
</style>