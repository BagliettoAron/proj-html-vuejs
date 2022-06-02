<template>
  <section class="header">
    <div class="header-top">
      <div class="big-container">
        <div>
          <i class="fas fa-clock"></i><span> {{ info.openTimeTables }} </span>
        </div>

        <div class="top-right">
          <i class="fas fa-phone"></i> <span> {{ info.phoneNumber }}</span>
          <i class="fas fa-envelope"></i> <span>{{ info.emailAdress }}</span>
          <i class="fab fa-facebook-f"></i>
          <i class="fab fa-twitter"></i>
          <i class="fab fa-linkedin-in"></i>
        </div>
      </div>
    </div>

    <div class="header-bottom">
      <div class="big-container">
        <div class="bottom-left">
          <span class="titleHighligts"> nex </span>
          <span class="titleGrey"> Gen </span>
        </div>

        <div class="bottom-right">
          <div class="navItem" v-for="(navItem, i) in nav" :key="i">
            <span>{{ navItem }}</span>
          </div>
          <i class="far fa-user"></i>
          <button>get in touch</button>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: "AppHeader",
  props: {
    info: Object,
    nav: Array,
  },
};
</script>

<style lang="scss" scoped>
@import "../style/common.scss";
@import "../style/variables.scss";
@import "../style/mixin.scss";

.header {
  width: 100%;
  height: 4rem;
  position: relative;

  .header-top {
    position: absolute;
    background-color: $bg-header-top-color;
    width: 100%;
    height: 4rem;
    top: 0;
    left: 0;
    color: $grey-text-color;
    font-size: 0.8rem;
    font-weight: 500;

    .top-right {
      span,
      i {
        padding: 0 0.5rem;
      }
    }
  }

  .big-container {
    display: flex;
    justify-content: space-between;
    align-items: center;
    height: 4rem;
  }

  .header-bottom {
    position: absolute;
    width: 100%;
    height: 4rem;
    bottom: -4rem;
    left: 0;
    z-index: 1;

    .bottom-left {
      .titleHighligts {
        text-transform: uppercase;
        background-color: $nexgen-bg-color-trasparency;
        padding: 0.3rem 0 0.3rem 1rem;
        border-radius: 45% 0 0 45%;
        margin-right: 0.3rem;
        font-weight: 500;
        color: $nexgen-txt-color;
      }

      .titleGrey {
        text-transform: uppercase;
        font-weight: 500;
        color: $grey-text-color;
      }
    }

    .bottom-right {
      text-transform: uppercase;
      color: $grey-text-color;
      display: flex;
      align-items: center;

      span {
        padding: 0 0.5rem;
        font-weight: 500;
      }
      i {
        padding: 0 0.5rem;
        font-weight: 500;
      }

      button {
        @include button--solid();
        margin: 0 0.5rem;
      }
    }
  }
}


</style>
