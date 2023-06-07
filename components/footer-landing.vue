<template>
  <div style="background: #07477a; padding-bottom: 100px; position: relative">
    <b-img
      :src="require('~/assets/images/background-footer.png')"
      style="
        position: absolute;
        bottom: 0;
        right: 0;
        left: 0;
        width: 100%;
        height: 200px;
      "
    ></b-img>
    <b-row no-gutters>
      <b-col md="4">
        <div class="pt-4 px-4">
          <b-img :src="require('~/assets/images/logo-test-white.png')"></b-img>
        </div>
      </b-col>
      <b-col md="4">
        <div class="px-4">
          <div class="mt-4 p-4" style="background: #ffffff; min-height: 245px">
            <b-form-select
              v-model="selected"
              :options="options"
            ></b-form-select>
            <p class="mt-5" style="color: #25a0d8">
              Jl. Lembong No 8 Kel. Braga Kec. Sumur Bandung, Kota Bandung, Jawa
              Barat
            </p>
          </div>
        </div>
      </b-col>
      <b-col md="4">
        <div class="px-4 pt-4">
          <p class="text-white">Who We Are</p>
          <p class="text-white">Our Values</p>
          <p class="text-white">The Perks</p>
        </div>
      </b-col>
    </b-row>
  </div>
</template>

<script>
export default {
  data() {
    return {
      selected: "TECHNOLOGY DEPARTMENT",
      options: [
        {
          value: "TECHNOLOGY DEPARTMENT",
          text: "TECHNOLOGY DEPARTMENT",
        },
      ],
    };
  },
};
</script>

<style>
</style>