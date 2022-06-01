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

    <!-- LATEST NEWS SECTION -->
    <AppSection5 />
    <!-- / LATEST NEWS SECTION -->

    <!-- KNOW FIRST SECTION -->
    <AppSection6 />
    <!-- / KNOW FIRST SECTION -->

    <!-- GET IN TOUCH SECTION -->
    <AppSection7 />
    <!-- GET IN TOUCH SECTION -->

  </div>    
</template>

<script>
import AppSection1 from "./main-components/AppSection1.vue";
import AppSection2 from "./main-components/AppSection2.vue";
import AppSection3 from "./main-components/AppSection3.vue";
import AppSection4 from "./main-components/AppSection4.vue";
import AppSection5 from "./main-components/AppSection5.vue";
import AppSection6 from "./main-components/AppSection6.vue";
import AppSection7 from "./main-components/AppSection7.vue";


export default {
  name: "AppMain",
  components: {
    AppSection1,
    AppSection2,
    AppSection3,
    AppSection4,
    AppSection5,
    AppSection6,
    AppSection7
  }
};
</script>

<style lang="scss" scoped></style>
