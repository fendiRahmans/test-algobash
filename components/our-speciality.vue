<template>
  <div style="background: #509fdd; min-height: 100px; padding: 20px;;">
    <div class="bg-white pt-4 px-4 pb-5" style="min-height: 100px; overflow: hidden">
      <p class="text-title text-blue text-center">OUR SPECIALITY</p>
      <p class="text-gray text-center">
        Lorem ipsum dolor sit amet, consectetur adipiscing elit. Duis euismod
        libero vel leo auctor, in venenatis nulla consequat. Sed commodo nunc
        sit amet congue aliquam.
      </p>
      <div class="d-flex justify-content-center">
        <b-img
          v-if="currentContent !== 1"
          :src="require('~/assets/images/' + content[currentContent - 2].image)"
          style="filter: blur(4px)"
        ></b-img>
        <div
          class="d-flex flex-column justify-content-center mx-5"
          style="width: max-content"
        >
          <b-img
            :src="
              require('~/assets/images/' + content[currentContent - 1].image)
            "
          ></b-img>
          <p class="mt-2 text-center">
            {{ content[currentContent - 1].title }}
          </p>
        </div>
        <b-img
          v-if="currentContent !== 3"
          :src="require('~/assets/images/' + content[currentContent].image)"
          style="filter: blur(4px)"
        ></b-img>
      </div>
      <p class="text-gray text-center mt-4">
        {{ content[currentContent - 1].description }}
      </p>
      <div
        class="d-flex justify-content-center align-items-center mx-auto"
        style="max-width: 323px; min-height: 10vh"
      >
        <i
          @click="previosContent()"
          :class="
            currentContent !== 1 ? 'arrow-active pointer' : 'arrow-disable'
          "
          class="fa fa-arrow-left"
        ></i>
        <div class="mx-5 d-flex">
          <div
            v-for="(item, index) in content"
            :key="index"
            class="mx-2"
            :class="
              currentContent - 1 !== index
                ? 'item-carosel'
                : 'active-item-carosel'
            "
          ></div>
        </div>
        <i
          @click="nextContent()"
          :class="
            currentContent !== content.length
              ? 'arrow-active pointer'
              : 'arrow-disable'
          "
          class="fa fa-arrow-right"
        ></i>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      currentContent: 1,
      content: [
        {
          image: "Accesories.svg",
          title: "Accesories",
          description:
            "Lorem ipsum dolor sit amet, consectetur adipiscing elit. Duis euismod libero vel leo auctor, in venenatis nulla consequat. Sed commodo nunc sit amet congue aliquam.",
        },
        {
          image: "Speed Improvement.svg",
          title: "Speed Improvement",
          description:
            "Nam libero tempore, cum soluta nobis est eligendi optio cumque nihil impedit quo minus id quod maxime placeat.",
        },
        {
          image: "Exhaust.svg",
          title: "Exhaust",
          description:
            "At vero eos et accusamus et iusto odio dignissimos ducimus qui blanditiis praesentium voluptatum deleniti atque.",
        },
      ],
    };
  },
  methods: {
    nextContent() {
      if (this.currentContent < this.content.length) {
        this.currentContent += 1;
      }
    },
    previosContent() {
      if (this.currentContent > 1) {
        this.currentContent -= 1;
      }
    },
  },
};
</script>

<style>
</style>