<template>
  <div style="min-height: 20vh; background: #f8f8f8">
    <div style="padding: 40px">
      <p class="text-blue text-title text-center mb-4">Our Core Values</p>
      <p class="text-gray">
        Ridiculus laoreet libero pretium et, sit vel elementum convallis fames.
        Sit suspendisse etiam eget egestas. Aliquet odio et lectus etiam sit.
      </p>
      <p class="text-gray">
        In mauris rutrum ac ut volutpat, ornare nibh diam. Montes, vitae, nec
        amet enim.
      </p>
      <div v-for="(item, index) in content" :key="index" class="mb-3">
        <div class="d-flex align-items-center">
          <div
            class="mr-3"
            style="background: #747474; height: 2px; width: 26px"
          ></div>
          <div style="font-size: 24px">{{ item.title }}</div>
        </div>
        <div style="margin-left: 44px">
          {{ item.desctiptopn }}
        </div>
      </div>
    </div>
    <div class="d-flex justify-content-end">
      <b-img
        :src="require('~/assets/images/ilustrasi-1.png')"
        style="width: auto; height: 250px"
      ></b-img>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      content: [
        {
          title: "Dedication",
          desctiptopn:
            "Nam libero tempore, cum soluta nobis est eligendi optio cumque nihil impedit quo minus id quod maxime placeat.",
        },
        {
          title: "Intellectual Honesty",
          desctiptopn:
            "Itaque earum rerum hic tenetur a sapiente delectus, ut aut reiciendis voluptatibus maiores alias conse.",
        },
        {
          title: "Curiosity",
          desctiptopn:
            "At vero eos et accusamus et iusto odio dignissimos ducimus qui blanditiis praesentium voluptatum deleniti atque.",
        },
      ],
    };
  },
};
</script>

<style>
</style>