<template>

  <div>
    <!-- FINANCIAL RISK SECTION -->
  <AppSection1 />
    <!-- / FINANCIAL RISK SECTION -->

  <!-- ADVISORY PERFORMANCE & RESULTS IN NUMBERS SECTION -->
  <AppSection2 />
  <!-- / ADVISORY PERFORMANCE & RESULTS IN NUMBERS SECTION -->

  </div>
</template>

<script>
import AppSection1 from "./main-components/AppSection1.vue"
import AppSection2 from "./main-components/AppSection2.vue"


export default {
  name: "AppMain",
  components: {
      AppSection1,
      AppSection2
  }
};
</script>

<style lang="scss" scoped>

</style>
