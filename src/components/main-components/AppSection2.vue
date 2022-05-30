<template>
<section class="big-container">

<div class="advisoryPerformance">
<div class="advisoryPerformance__content small-container">
<small>introduction video</small>
<h2><span class="grey-title">Advisory</span>  <span class="highlight-title" >Performance</span> </h2>
<p class="grey-text"> Financials executives need to review their strategies, operating models and capabilities so that their areas can generate sound information for better decision making.</p>
<img :src="require('../../assets/img/video-1.jpg')" alt="">

</div>

  <i class="fad fa-play"></i>

</div>

</section>
  
</template>

<script>

export default {
    name: 'AppSection2',

}

</script>

<style lang="scss" scoped>
@import "../../style/common.scss";
@import "../../style/variables.scss";
@import "../../style/mixin.scss";

.advisoryPerformance{
    width: 100%;
    position: relative;
    height: 40rem;

    &__content{
    @include toCenter();
    }

    small{
        text-transform: uppercase;
        color: $button-solid-color;
        font-weight: 550;
    }

    h2{
        font-size: 2rem;
        padding: 2rem 0;
        .grey-title{
            color: $grey-title-color;
        }

        .highlight-title{
            color: $highlight-title-color;
            background-color: $highlight-title-background;
        }

    }

    img {
        width: 100%;
        padding: 2rem 0;
  
    }

    i{
        color: black;
    }



}




</style>