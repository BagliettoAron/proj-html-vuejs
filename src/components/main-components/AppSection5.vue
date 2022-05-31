<template>
  <section class="latestNews">
    <div class="big-container">
      <div class="title-section">
        <small>our editorial content</small>
        <h2>
          <span class="grey-title">Latest</span>
          <span class="highlight-title">News</span>
        </h2>
        <div class="text-and-button">
          <p class="grey-text">
            Every week we pubblish content about what is best in the business
            world.
            <button>see all</button>
          </p>
        </div>
      </div>
      <div class="card-section">
        <div class="card">
          <img src="../../assets/img/news-1.jpg" alt="" />
          <h4>increasing creativity is possible for everyone</h4>
        </div>
        <div class="card">
          <img src="../../assets/img/news-2.jpg" alt="" />
          <h4>Because market research is part of the business plan</h4>
        </div>
        <div class="card">
          <img src="../../assets/img/news-3.jpg" alt="" />
          <h4>Working from home is now a trend</h4>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: "AppSection5",
};
</script>

<style lang="scss" scoped>
@import "../../style/common.scss";
@import "../../style/variables.scss";
@import "../../style/mixin.scss";

.latestNews {
  width: 100%;
  background-color: $latestNews-section-background;
  padding: 4rem 0;

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
}

.text-and-button {
  display: flex;

  button {
    @include button--solid();
    width: 5rem;
    margin-left: 3rem;
    padding: 0.5rem 0rem;
  }
}

.card-section {
  display: flex;
  padding: 2rem 0;

  .card {
    width: calc(100% / 3 - 14px);
    margin: 7px;
    position: relative;
    overflow: hidden;

    img {
      width: 100%;
      border-radius: 5px;
      filter: brightness(0.5);
    }

    h4 {
      position: absolute;
      left: 50%;
      bottom: 5%;
      transform: translate(-50%, -50%);
      width: 90%;
      text-align: center;
      color: $financial-risk-title-color;
    }
  }
}
</style>
