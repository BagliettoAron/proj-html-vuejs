<template>
  <section class="teamOfExperts">
    <div class="big-container">
      <div class="left-side">
        <small>introduction video</small>
        <h2>
          <span class="highlight-title">Team</span>
          <span class="grey-title">of Experts</span>
        </h2>
        <div class="text-and-button">
          <p class="grey-text">
            Financials executives need to review their strategies, operating
            models and capabilities so that their areas can generate sound
            information for better decision making.
          </p>
        </div>

        <div class="card-container">
            <div class="card">
                <div class="leftSide-card">
                <img src="../../assets/img/team-1.jpg" alt="David Cooper">
                </div>

                <div class="rightSide-card">
                
                </div>
            </div>
        </div>
      </div>

      <div class="right-side">
        <h3>President Speech</h3>
        <p>
          Lorem ipsum dolor sit amet consectetur adipisicing elit. Voluptas
          voluptatum natus recusandae.
        </p>
        <p>
          Lorem ipsum dolor sit amet consectetur adipisicing elit. Dicta ipsa
          quam praesentium soluta dignissimos consectetur, voluptatibus
          provident, nisi sint commodi et mollitia cum nobis similique quaerat.
          Non quisquam accusantium sit?
        </p>
        <p>
          Lorem ipsum dolor sit amet consectetur adipisicing elit. Laborum
          temporibus reiciendis voluptates et id sint.
        </p>
        <div class="authorAndIcon">
          <h4>T.Johnson</h4>
          <i class="fas fa-quote-right"></i>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: "AppSection4",
};
</script>

<style lang="scss" scoped>
@import "../../style/common.scss";
@import "../../style/variables.scss";
@import "../../style/mixin.scss";

.teamOfExperts {
  width: 100%;
  padding: 4rem 0;
  height: 50rem;

  .left-side {
    width: 75%;
    float: left;

    small {
      @include smallTitle();
    }

    h2 {
      @include h2SubTitle();
      padding: 1.5rem 0rem;
    }

    .highlight-title {
      @include highLightTitle();
      color: $highlight-title-color;
      margin-right: 0.5rem;
    }

    .grey-title {
      color: $grey-title-color;
      margin-right: 0.5rem;
    }
  }

  .right-side {
    width: 25%;
    background-color: $highlight-title-color;
    height: 30rem;
    float: left;
    padding: 1.5rem;
    border-radius: 5px;

    h3 {
      color: $financial-risk-title-color;
      padding-bottom: 2rem;
    }

    p {
      font-size: 0.8rem;
      color: $predidentSpeech-color;
      padding-bottom: 1rem;
    }

    .authorAndIcon {
      display: flex;
      justify-content: space-between;
      padding-top: 3rem;

      h4 {
        color: $predidentSpeech-color;
      }

      i {
        font-size: 1.5rem;
        color: $quote-right-icon-color;
      }
    }
  }
}
</style>
