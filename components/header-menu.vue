<template>
  <div>
    <b-navbar toggleable="lg">
      <b-navbar-brand>
        <b-img
          fluid
          :src="require('~/assets/images/logo-test.png')"
          style="width: 160px"
        ></b-img>
      </b-navbar-brand>
      <b-navbar-toggle target="nav-collapse"></b-navbar-toggle>
      <b-collapse id="nav-collapse" is-nav>
        <!-- Right aligned nav items -->
        <b-navbar-nav class="ml-auto">
          <b-nav-item v-for="item in 3" :key="item" href="#">Link</b-nav-item>
        </b-navbar-nav>
      </b-collapse>
    </b-navbar>
  </div>
</template>

<script>
export default {};
</script>

<style>
</style>