<template>
  <div>
    <!-- FINANCIAL RISK SECTION -->
    <AppSection1 />
    <!-- / FINANCIAL RISK SECTION -->

    <!-- ADVISORY PERFORMANCE & RESULTS IN NUMBERS SECTION -->
    <AppSection2 />
    <!-- / ADVISORY PERFORMANCE & RESULTS IN NUMBERS SECTION -->

    <!-- EXCELLENCE IN SERVICES SECTION -->
    <AppSection3 />
    <!-- / EXCELLENCE IN SERVICES SECTION -->

    <!-- TEAM OF EXPERTS SECTION -->
    <AppSection4 />
    <!-- / TEAM OF EXPERTS SECTION -->

  </div>
</template>

<script>
import AppSection1 from "./main-components/AppSection1.vue";
import AppSection2 from "./main-components/AppSection2.vue";
import AppSection3 from "./main-components/AppSection3.vue";
import AppSection4 from "./main-components/AppSection4.vue";

export default {
  name: "AppMain",
  components: {
    AppSection1,
    AppSection2,
    AppSection3,
    AppSection4,

  },
};
</script>

<style lang="scss" scoped></style>
