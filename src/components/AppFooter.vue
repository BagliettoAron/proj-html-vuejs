<template>
  <section class="footer">
    <div class="big-container">
      <div class="card-wrapper">
        <div class="card-menu left-menu">
          <div class="titleLogo">
            <span class="titleHighligts"> nex </span>
            gen
          </div>
          <p>A functional HTML template for Corporate & Business.</p>
          <span class="iconText"
            ><i class="fas fa-phone"></i> +01 (305) 1234-5678</span
          >
          <span class="iconText"
            ><i class="fas fa-envelope"></i>hello@example.com</span
          >
          <span class="iconText"
            ><i class="fas fa-map-marker-alt"></i>Main Avenue, 987</span
          >
          <button>Get in Touch</button>
        </div>

        <div class="card-menu">
          <div class="cardContent">
            <h3>title</h3>
            <ul>
              <li><i class="fas fa-chevron-right"></i>adefbadf</li>
              <li><i class="fas fa-chevron-right"></i>sdfbbfd</li>
              <li><i class="fas fa-chevron-right"></i>sbgsfgb</li>
              <li><i class="fas fa-chevron-right"></i>sfgbsfbg</li>
              <li><i class="fas fa-chevron-right"></i>sfrbg</li>
              <li><i class="fas fa-chevron-right"></i>gfbs</li>
            </ul>
          </div>
        </div>

         <div class="card-menu">
          <div class="cardContent">
            <h3>title</h3>
            <ul>
              <li><i class="fas fa-chevron-right"></i>adefbadf</li>
              <li><i class="fas fa-chevron-right"></i>sdfbbfd</li>
              <li><i class="fas fa-chevron-right"></i>sbgsfgb</li>
              <li><i class="fas fa-chevron-right"></i>sfgbsfbg</li>
              <li><i class="fas fa-chevron-right"></i>sfrbg</li>
              <li><i class="fas fa-chevron-right"></i>gfbs</li>
            </ul>
          </div>
        </div>

         <div class="card-menu">
          <div class="cardContent">
            <h3>title</h3>
            <ul>
              <li><i class="fas fa-chevron-right"></i>adefbadf</li>
              <li><i class="fas fa-chevron-right"></i>sdfbbfd</li>
              <li><i class="fas fa-chevron-right"></i>sbgsfgb</li>
              <li><i class="fas fa-chevron-right"></i>sfgbsfbg</li>
              <li><i class="fas fa-chevron-right"></i>sfrbg</li>
              <li><i class="fas fa-chevron-right"></i>gfbs</li>
            </ul>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: "AppFooter",
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

  .big-container {
    padding: 7rem 0;

    .card-wrapper {
      display: flex;
      justify-content: space-between;
    }

    .card-menu {
      width: calc(100% / 4 - 20px);
      margin: 10px;
      min-height: 15rem;

      .cardContent {
        padding: 1rem;
        border-radius: 5px;
        background-color: $footer-bg-grey-cards;
        min-height: 15rem;

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
          background-color: $button-solid-color;
          padding: 0.3rem 0 0.3rem 0.7rem;
          border-radius: 10px 0 0 10px;
          margin-right: 0.3rem;
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

      button {
        @include button--empty();
        width: 80%;
        color: $button-solid-color;
        font-size: 0.6rem;
      }
    }
  }
}
</style>
