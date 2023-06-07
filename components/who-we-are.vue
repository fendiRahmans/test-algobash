<template>
  <div class="" style="padding: 40px">
    <p class="text-title text-blue mb-4">
      {{ content[currentContent - 1].title }}
    </p>
    <p class="text-subtitle mb-1">{{ content[currentContent - 1].subtitle }}</p>
    <p class="text-content text-gray">
      {{ content[currentContent - 1].description }}
    </p>
    <b-row align-v="center" class="mt-5">
      <b-col cols>
        <p class="mb-0">
          <span style="color: #303030; font-size: 24px"
            >0{{ currentContent }}</span
          >
          <span style="font-size: 24px; color: #c0c0c0">/</span>
          <span style="color: #c0c0c0; font-size: 16px"
            >0{{ content.length }}</span
          >
        </p>
      </b-col>
      <b-col cols="auto">
        <div class="d-flex">
          <div
            @click="previosContent()"
            :class="currentContent !== 1 ? 'button-active pointer' : 'button-disable'"
            class=" d-flex align-items-center justify-content-center"
          >
            <i class="fa fa-arrow-left" style="font-size: 30px"></i>
          </div>
          <div
            @click="nextContent()"
            :class="
              currentContent !== content.length
                ? 'button-active pointer'
                : 'button-disable'
            "
            class="button-next d-flex align-items-center justify-content-center"
          >
            <i class="fa fa-arrow-right" style="font-size: 30px"></i>
          </div>
        </div>
      </b-col>
    </b-row>
  </div>
</template>

<script>
export default {
  data() {
    return {
      currentContent: 1,
      content: [
        {
          id: 1,
          title: "Who we are",
          subtitle: "Technology Company",
          description:
            "Sed ut perspiciatis unde omnis iste natus sit voluptatem accusantium doloremque laudantium, totam rem aperiam, eaque ipsa quae ab illo inventore veritatis et quasi architecto beatae vitae dicta sunt explicabo.",
        },
        {
          id: 2,
          title: "What we do",
          subtitle: "Professional Brand Management",
          description:
            "Neque porro quisquam est, qui dolorem ipsum quia dolor sit amet, consectetur, adipisci velit, sed quia non numquam eius modi tempora incidunt ut labore et dolore magnam aliquam quaerat voluptatem.",
        },
        {
          id: 3,
          title: "How we do",
          subtitle: "Strategize, Design, Collaborate",
          description:
            "Ut enim ad minima veniam, quis nostrum exercitationem ullam corporis suscipit laboriosam, nisi ut aliquid ex ea commodi consequatur? Quis autem vel eum iure reprehenderit qui in ea voluptate velit esse sequam nihil molestiae consequatur.",
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