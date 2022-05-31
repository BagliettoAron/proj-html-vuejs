<template>
  <section class="knowFirst">
    <div class="big-container">
      <div class="small-container">
        <div class="left-side">
          <small>newsletter</small>
          <h2>
            <span class="highlight-title">Know</span>
            <span class="grey-title">First</span>
          </h2>
          <div class="text-and-button">
            <p class="grey-text">
              Follow closely and receive content about our company and the news of the current market.
            </p>
          </div>
        </div>

        <div class="right-side">
        <input type="text" placeholder="Name">
        <input type="email" placeholder="Email">
        <button>subscribe</button>

        
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: "AppSection6",
};
</script>

<style lang="scss" scoped>
@import "../../style/common.scss";
@import "../../style/variables.scss";
@import "../../style/mixin.scss";

.knowFirst {
  width: 100%;
  background-color: $excellence-background;
  padding: 4rem 0;

    .small-container{
        display: flex;

  .left-side {
    width: 50%;

    small {
      @include smallTitle();
    }

    h2 {
      @include h2SubTitle();
      padding: 1.5rem 0rem;
    }

    .highlight-title {
      @include highLightTitle();
      color: $financial-risk-title-color;
      margin-right: .5rem;
    }

    .grey-title {
      color: $financial-risk-title-color;
      margin-right: 0.5rem;
    }
  }

    }

  .right-side{
      width: 50%;
      display: flex;
      flex-direction: column;
      justify-content: space-between;
      margin-left: 1rem;

      input{
          background-color: $excellence-card-background;
          height: calc(100% / 3 - 20px);
          margin: 10px;
          border: none;
          padding-left: 1rem;
          border-radius: 5px;
      }

      button{
          @include button--solid();
          width: 8rem;
          margin: 10px;
      }
  }


}
</style>
