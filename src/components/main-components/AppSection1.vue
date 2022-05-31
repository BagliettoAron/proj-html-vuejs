<template>
  <section class="financialRisk">
    <div class="">
      <!-- title, paragraph and buttons -->
      <div class="financialRisk__bottom big-container">
        <div class="financialRisk__bottom__titleSection small-container">
          <h2>Financial Risk</h2>
          <p class="grey-text">
            The right outcomes depend on continuos rigor in governance, models
            and processes across the finance function.
          </p>
          <button class="button--solid">get in touch</button>
          <button class="button--empty">read more</button>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: "AppSection1",
};
</script>

<style lang="scss" scoped>
@import "../../style/common.scss";
@import "../../style/variables.scss";
@import "../../style/mixin.scss";

.financialRisk {
  width: 100%;
  height: 50rem;
  background-image: url("../../assets/img/bg-2.jpg");
  background-size: cover;
  background-repeat: no-repeat;
  background-position: center;
  position: relative;

  &__bottom {
    @include toCenter();

    &__titleSection {
      h2 {
        color: $financial-risk-title-color;
        font-weight: 800;
        font-size: 2.5rem;
      }

      p {
        padding: 2rem 0;
      }

      .button--solid {
        @include button--solid();
        margin-right: 1rem;
      }

      .button--empty {
        @include button--empty();
      }
    }
  }
}
</style>
