<template>
  <div class="">
    <section class="big-container">
      <div class="advisoryPerformance">
        <div class="advisoryPerformance__content small-container">
          <small>introduction video</small>
          <h2>
            <span class="grey-title">Advisory</span>
            <span class="highlight-title">Performance</span>
          </h2>
          <p class="grey-text">
            Financials executives need to review their strategies, operating
            models and capabilities so that their areas can generate sound
            information for better decision making.
          </p>
          
          <div class="img-logoPlay">
          <img :src="require('../../assets/img/video-1.jpg')" alt="video do something great" />
          <i class="fas fa-play "></i>
          </div>
          
         
        </div>

      </div>
    </section>

    <section class="results-section">
      <div class="resultsNumbers big-container">
        <div class="resultsNumbers__content small-container">
          <small>what are we doing</small>
          <h2>
            <span class="highlight-title">Results</span>
            <span class="grey-title">in Numbers</span>
          </h2>
          <div class="skills">
            <div
              class="skills__score"
              v-for="(ratings, i) in scoreSkills"
              :key="i"
            >
              <div class="skills__score__numberOf">{{ ratings.score }}</div>
              <div class="skills__score__item">{{ ratings.skill }}</div>
            </div>
          </div>
        </div>
      </div>
    </section>
  </div>
</template>

<script>
export default {
  name: "AppSection2",
  data: function () {
    return {
      scoreSkills: [
        {
          score: "128",
          skill: "Certification",
        },
        {
          score: "230",
          skill: "Employees",
        },
        {
          score: "517",
          skill: "Customers",
        },
        {
          score: "94",
          skill: "Countries Served",
        },
      ],
    };
  },
};
</script>

<style lang="scss" scoped>
@import "../../style/common.scss";
@import "../../style/variables.scss";
@import "../../style/mixin.scss";
@import "~@fortawesome/fontawesome-free/css/all.min.css";

.advisoryPerformance {
  width: 100%;
  position: relative;
  height: 50rem;

  &__content {
    @include toCenter();
  }

  small {
    @include smallTitle();
  }

  h2 {
    @include h2SubTitle();
  }

  .highlight-title {
    @include highLightTitle();
  }

  .grey-title {
    color: $grey-title-color;
    margin-right: 0.5rem;
  }

  .img-logoPlay{
    position: relative;
  }

  i{
    position: absolute;
    left: 50%;
    top: 50%;
    transform: translate(-50%, -50%);
    color: $icon-play-trasparency-color;
    font-size: 5rem;
    text-shadow: 0px -8px $icon-play-trasparency-color-shadow;

  }


}

img {
  width: 100%;
  padding: 2rem 0;
}

i {
  color: black;
}

.results-section {
  background-image: url("../../assets/img/bg-7.jpg");


}

.resultsNumbers {
  width: 100%;
  height: 30rem;
  position: relative;

  &__content {
    @include toCenter();
  }

  small {
    @include smallTitle();
  }

  h2 {
    @include h2SubTitle();
  }

  .grey-title {
    color: $financial-risk-title-color;
    margin-right: 0.5rem;
  }

  .highlight-title {
    @include highLightTitle();
    margin-right: 0.5rem;
    color: $financial-risk-title-color;
  }

  .skills {
    display: flex;
    justify-content: space-around;

    &__score__numberOf {
      color: $score-numbers-color;
      font-size: 2rem;
      font-weight: 550;
    }

    &__score__item {
      padding-top: 1rem;
      color: $financial-risk-title-color;
      font-weight: 550;
      font-size: 1.3rem;
    }
  }
}
</style>
