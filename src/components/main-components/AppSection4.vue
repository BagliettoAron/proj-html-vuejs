<template>
  <section class="teamOfExperts">
    <div class="big-container">
      <div class="left-side">
        <small>we like what we do</small>
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
          <div class="card" v-for="(teamMember, i) in teamCards" :key="i">
            <div class="leftSide-card">
              <img
                :src="require(`../../assets/img/${teamMember.image}.jpg`)"
                :alt="teamMember.name"
              />
            </div>

            <div class="rightSide-card">
              <h4>{{ teamMember.name }}</h4>
              <p>{{ teamMember.assignement }}</p>
              <ul>
                <li><i :class="teamMember.social1"></i></li>
                <li><i :class="teamMember.social2"></i></li>
                <li><i :class="teamMember.social3"></i></li>
              </ul>
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
  data: function () {
    return {
      teamCards: [
        {
          image: "team-1",
          name: "David Cooper",
          assignement: "cto & co-founder",
          social1: "fab fa-facebook",
          social2: "fab fa-twitter",
          social3: "fab fa-linkedin-in",
        },
        {
          image: "team-3",
          name: "Oliver Jones",
          assignement: "chief procurement",
          social1: "fab fa-facebook",
          social2: "fab fa-twitter",
          social3: "fab fa-linkedin-in",
        },
        {
          image: "team-2",
          name: "Emma Lopez",
          assignement: "chief marketing",
          social1: "fab fa-facebook",
          social2: "fab fa-twitter",
          social3: "fab fa-linkedin-in",
        },
        {
          image: "team-4",
          name: "T. Johnson",
          assignement: "ceo & president",
          social1: "fab fa-facebook",
          social2: "fab fa-twitter",
          social3: "fab fa-linkedin-in",
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

.big-container {
  display: flex;
}

.teamOfExperts {
  width: 100%;
  padding: 5rem 0;

  .left-side {
    width: 70%;

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

    .card-container {
      display: flex;
      flex-wrap: wrap;
      margin-top: 2rem;

      .card {
        width: calc(100% / 2 - 10px);
        margin: 5px;

        .leftSide-card {
          width: 40%;
          float: left;

          img {
            width: 100%;
            border-radius: 5px;
          }
        }

        .rightSide-card {
          width: 60%;
          float: left;

          padding-left: 1rem;
          padding-top: 1rem;

          p {
            text-transform: uppercase;
            color: $grey-title-color;
            font-size: 0.6rem;
            padding-top: 1rem;
          }

          ul {
            display: flex;
            justify-content: flex-start;
            padding-top: 1.5rem;

            li {
              padding-right: 0.5rem;

              i {
                width: 35px;
                height: 35px;
                border-radius: 50%;
                text-align: center;
                line-height: 35px;
                background-color: $highlight-title-background;
                color: $highlight-title-color;
                display: inline-block;
              }
            }
          }
        }
      }
    }
  }

  .right-side {
    width: 30%;
    background-color: $highlight-title-color;
    padding: 2rem;
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
