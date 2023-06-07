<template>
  <div>
    <cover />
    <who-we-are id="who-we-are" />
    <our-core-values />
    <our-speciality />
    <footer-landing />
  </div>
</template>

<script>
import cover from "~/components/cover.vue";
import FooterLanding from "~/components/footer-landing.vue";
import OurCoreValues from "~/components/our-core-values.vue";
import OurSpeciality from "~/components/our-speciality.vue";
import WhoWeAre from "~/components/who-we-are.vue";
export default {
  name: "IndexPage",
  components: { cover, WhoWeAre, OurCoreValues, OurSpeciality, FooterLanding },
};
</script>
