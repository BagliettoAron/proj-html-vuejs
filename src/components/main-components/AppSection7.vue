<template>
  <section class="getInTouch">
    <div class="big-container">
      <div class="content">
        <div class="left-side">
          <div class="title-section">
            <small>send a message</small>
            <h2>
              <span class="grey-title">Get in</span>
              <span class="highlight-title">Touch</span>
            </h2>
            <div class="text-and-button">
              <p class="grey-text">
                We will respond to your message as soon as possible.
              </p>
            </div>
          </div>
          <div class="form-sectionTop">
            <input type="text" placeholder="Name" />
            <input type="email" placeholder="Email" />
            <input type="number" placeholder="Phone" />
            <input type="text" placeholder="More Info" />
          </div>
          <div class="form-sectionBottom">
            <input type="text" placeholder="Message" />
          </div>
          <button class="sendButton">send</button>
        </div>
        <div class="right-side">
          <h3>Example Inc.</h3>
          <p>
            Lorem ipsum dolor sit amet consectetur adipisicing elit. Fuga
            debitis quam vel nam, aut totam voluptatibus.
          </p>
          <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit.</p>
          <span><i class="fas fa-phone"></i> +01 (305) 1234-5678</span>
          <span><i class="fas fa-envelope"></i>hello@example.com</span>
          <span><i class="fas fa-map-marker-alt"></i>Main Avenue, 987</span>
          <button>view map</button>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: "AppSection7",
};
</script>

<style lang="scss" scoped>
@import "../../style/common.scss";
@import "../../style/variables.scss";
@import "../../style/mixin.scss";

.getInTouch {
  width: 100%;
  padding: 4rem 0;

  .content {
    display: flex;

    .left-side {
      width: 65%;
      padding-right: 2rem;
      small {
        @include smallTitle();
      }

      h2 {
        @include h2SubTitle();
        padding: 1.5rem 0rem;
      }

      .highlight-title {
        @include highLightTitle();
      }

      .grey-title {
        color: $grey-title-color;
        margin-right: 0.5rem;
      }

      .form-sectionTop {
        display: flex;
        flex-wrap: wrap;
        justify-content: space-between;
        padding-top: 3rem;

        input {
          width: calc(100% / 2 - 10px);
          margin: 5px;
          border: none;
          background-color: $form-bg-color;
          padding: 0.7rem;
          border-radius: 5px;
        }
      }

      .form-sectionBottom {
        input {
          width: calc(100% - 10px);
          margin: 5px;
          border: none;
          background-color: $form-bg-color;
          padding: 0.7rem 0 6rem 0.7rem;
          border-radius: 5px;
        }
      }

      .sendButton {
        @include button--solid();
        margin-top: 0.5rem;
      }
    }

    .right-side {
      width: 35%;
      padding: 1rem;
      display: flex;
      flex-direction: column;
      justify-content: space-between;
      margin-top: 5px;

      i {
        width: 35px;
        height: 35px;
        border-radius: 50%;
        text-align: center;
        line-height: 35px;
        background-color: $highlight-title-background;
        color: $highlight-title-color;
        display: inline-block;
        margin-right: 0.5rem;
      }

      span {
        font-size: 0.8rem;
        color: $button-solid-color;
      }

      p {
        font-size: 0.8rem;
        color: $grey-text-color;
      }

      button {
        @include button--empty();
        width: 7rem;
        color: $button-solid-color;
      }
    }
  }
}
</style>
