<template>
  <section class="footer">
    <div class="big-container section-menu">
      <div class="card-wrapper">
        <div class="card-menu left-menu">
          <div class="titleLogo">
            <span class="titleHighligts"> nex </span>
           <span> gen</span>
          </div>
          <p>A functional HTML template for Corporate & Business.</p>
          <span class="iconText"
            ><i class="fas fa-phone"></i> {{ contactData.phoneNumber }}</span
          >
          <span class="iconText"
            ><i class="fas fa-envelope"></i>{{ contactData.emailAdress }}</span
          >
          <span class="iconText"
            ><i class="fas fa-map-marker-alt"></i
            >{{ contactData.position }}</span
          >
          <button class="button--empty">Get in Touch</button>
        </div>

        <div class="card-menu" v-for="(item, i) in listItem" :key="i">
          <div class="cardContent">
            <h3>{{ item.title }}</h3>
            <ul v-for="(itemList, i) in item.listMenu" :key="i">
              <li><i class="fas fa-chevron-right"></i>{{ itemList }}</li>
            </ul>
          </div>
        </div>
      </div>
    </div>
    <div class="bottom-footer">
      <div class="big-container bottom-copyright">
        <span
          >Enjoy the low price. We are tracking any intention of piracy.</span
        >
        <span
          >&#169; 2020 NEXGEN is Proudly Powered by
          <span class="greenBottomFooter">Codings</span>.</span
        >
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: "AppFooter",
  props: {
    listItem: Array,
    contactData: Object,
  },
};
</script>

<style lang="scss" scoped>
@import "../style/common.scss";
@import "../style/variables.scss";
@import "../style/mixin.scss";

.footer {
  width: 100%;
  background-image: url("../assets/img/bg-7.jpg");
  background-size: cover;
  background-repeat: no-repeat;
  background-position: center;

  .section-menu {
    padding: 7rem 0;

    .card-wrapper {
      display: flex;
      justify-content: space-between;
    }

    .card-menu {
      width: calc(100% / 4 - 20px);
      margin: 10px;
      min-height: 14rem;

      .cardContent {
        padding: 1rem;
        border-radius: 5px;
        background-color: $footer-bg-grey-cards;
        min-height: 14rem;

        h3 {
          color: $financial-risk-title-color;
          padding: 0.5rem;
        }

        li {
          color: $grey-text-color;
          font-size: 0.6rem;
          line-height: 1.3rem;
        }

        i {
          font-size: 0.6rem;
          margin-right: 0.5rem;
        }
      }
    }

    .left-menu {
      display: flex;
      flex-direction: column;
      justify-content: space-between;
      margin-top: 5px;
      padding-right: 1rem;

      .titleLogo {
        text-transform: uppercase;
        margin-top: 1rem;
        color: $grey-text-color;
        font-weight: 600;

        .titleHighligts {
          text-transform: uppercase;
          background-color: $nexgen-bg-color-trasparency;
          padding: 0.3rem 0 0.3rem 1rem;
          border-radius: 45% 0 0 45%;
          margin-right: 0.3rem;
          color: $nexgen-txt-color;
        }
      }

      i {
        color: $grey-text-color;
        margin-right: 0.5rem;
      }

      .iconText {
        font-size: 0.6rem;
        color: $grey-text-color;
      }

      p {
        font-size: 0.8rem;
        color: $grey-text-color;
        width: 100%;
      }

      .button--empty {
        @include button--empty();
        width: 80%;
        color: $button-solid-color;
        font-size: 0.6rem;
      }

      .button--empty:hover {
        background-color: #058283;
        border: none;
        border: 1px solid $button-solid-color;
        color: white;
        font-size: 0.6rem;
      }
    }
  }
}

.bottom-footer {
  width: 100%;
  height: 4rem;
  background-color: $bg-color-footer-bottom;

  .bottom-copyright {
    display: flex;
    justify-content: space-between;
    line-height: 4rem;
    font-size: 0.7rem;
    color: $grey-text-color;

    .greenBottomFooter {
      color: $button-solid-color;
    }

    
  }
}
</style>
