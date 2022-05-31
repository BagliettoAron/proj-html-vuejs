<template>
  <section class="excellenceInService">
    <div class="big-container">
      <small>introduction video</small>
      <h2>
        <span class="grey-title">Excellence in</span>
        <span class="highlight-title">Services</span>
      </h2>
      <div class="text-and-button">
        <p class="grey-text">
          Financials executives need to review their strategies, operating
          models and capabilities so that their areas can generate sound
          information for better decision making.
        </p>
        <button>see all</button>
      </div>
      <div class="cardContainer">
        <div class="cardContainer__card" v-for="(cardItem, i) in card" :key="i">
          <div class="cardContainer__card__inner">
            <div class="icon">
              <i :class="`${cardItem.leftIcon}`"></i>
              <i :class="`${cardItem.rightIcon}`"></i>
            </div>
            <div class="card-title">
              <h4>{{cardItem.title}}</h4>
            </div>
            <p class="grey-text">
             {{cardItem.paragraph}}
            </p>
          </div>
        </div>
      
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: "AppSection3",
  data: function (){
      return{
          card : [
              {
                  leftIcon: "fas fa-network-wired",
                  rightIcon: "fas fa-arrow-right",
                  title: "Audit & Assurance",
                  paragraph: "Lorem ipsum dolor sit amet consectetur adipisicing elit."
              },
               {
                  leftIcon: "fas fa-briefcase",
                  rightIcon: "fas fa-arrow-right",
                  title: "Financial Advisory",
                  paragraph: "Lorem ipsum dolor sit amet consectetur adipisicing elit."
              },
               {
                  leftIcon: "fas fa-chart-bar",
                  rightIcon: "fas fa-arrow-right",
                  title: "Analytics and M&A",
                  paragraph: "Lorem ipsum dolor sit amet consectetur adipisicing elit."
              },
               {
                  leftIcon: "fas fa-plane",
                  rightIcon: "fas fa-arrow-right",
                  title: "Middle Marketing",
                  paragraph: "Lorem ipsum dolor sit amet consectetur adipisicing elit."
              },
               {
                  leftIcon: "fas fa-globe",
                  rightIcon: "fas fa-arrow-right",
                  title: "Legal Consulting",
                  paragraph: "Lorem ipsum dolor sit amet consectetur adipisicing elit."
              },
               {
                  leftIcon: "fas fa-archive",
                  rightIcon: "fas fa-arrow-right",
                  title: "Regulatory Risk",
                  paragraph: "Lorem ipsum dolor sit amet consectetur adipisicing elit."
              },
          ]
      }
  }
};
</script>

<style lang="scss" scoped>
@import "../../style/common.scss";
@import "../../style/variables.scss";
@import "../../style/mixin.scss";

.excellenceInService {
  width: 100%;
  background-color: $excellence-background;
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
    color: $financial-risk-title-color;
  }

  .grey-title {
    color: $financial-risk-title-color;
    margin-right: 0.5rem;
  }
}

.text-and-button {
  display: flex;

  button {
    @include button--empty();
    width: 10rem;
    margin-left: 3rem;
    padding: 0rem 0rem;
  }
}

.cardContainer {
  display: flex;
  justify-content: center;
  flex-wrap: wrap;
  padding: 3rem 0;

  &__card {
    width: calc(100% / 3 - 8px);
    margin: 4px;
    background-color: $excellence-card-background;
    height: 10rem;
    border-radius: 5px;
    overflow: hidden;
    padding: 1.5rem;

    &__inner {
      width: 100%;
      height: 100%;

      .icon {
        display: flex;
        justify-content: space-between;
        color: $button-solid-color;
        font-size: 1.5rem;
      }

      .card-title {
        color: $financial-risk-title-color;
        padding: 1rem 0;
        text-align: center;
      }

      p {
        font-size: 0.8rem;
        text-align: center;
      }
    }
  }
}
</style>
