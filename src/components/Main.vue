<template>
  <main class="resume--main">
    <card :cards="cards"></card>
    <card2 :cards="cards"></card2>
    <card3 :cards="cards"></card3>
    <card4 :cards="cards"></card4>
    <card5 :cards="cards"></card5>
    <card6 :cards="cards"></card6>
  </main>
</template>

<script>
import Card from "./cards/Card.vue";
import Card2 from "./cards/Card2.vue";
import Card3 from "./cards/Card3.vue";
import Card4 from "./cards/Card4.vue";
import Card5 from "./cards/Card5.vue";
import Card6 from "./cards/Card6.vue";
export default {
  data() {
    return {
      cards: [
        {
          caption: "Mountains",
          img: "../assets/img/Screenshot_2019-07-23 Document.png",
          code: "https://github.com/louiss0/Mountains",
          site: "https://mountains0.netlify.com"
        },
        {
          caption: "Stock Trader",
          img: "../assets/img/Screenshot_2019-07-23 Stock-trader.png",
          code: "https://github.com/louiss0/stock-trader",
          site: "https://stocktrade.netlify.com"
        },
        {
          caption: "Fast Pizza",
          img: "../assets/img/Screenshot_2019-07-23 Fast Pizza.png",
          code: "https://github.com/louiss0/Fast-Pizza",
          site: "https://fastpizza.netlify.com"
        },
        {
          caption: "Monster Slayer",
          img: "../assets/img/Screenshot_2019-07-23 Monster Slayer.png",
          code: "https://github.com/louiss0/monster-slayer",
          site: "https://monster-slayer.netlify.com"
        },
        {
          caption: "Users",
          img: "../assets/img/Screenshot_2019-07-23 users.png",
          code: "https://github.com/louiss0/users",
          site: "https://fiveusers.netlify.com"
        },
        {
          caption: "To Do List",
          img: "../assets/img/Screenshot_2019-07-23 ToDO List.png",
          code: "https://github.com/louiss0/To-Do-List",
          site: "https://totodo.netlify.com"
        }
      ]
    };
  },
  components: {
    card: Card,
    card2: Card2,
    card3: Card3,
    card4: Card4,
    card5: Card5,
    card6: Card6
  }
};
</script>

<style lang='scss'>
@import "../scss/abstracts.scss";
.resume {
  &--main {
    display: grid;
    grid-column-gap: 4em;
    grid-row-gap: 3em;
    grid-template-columns: repeat(auto-fit, 30em);
    justify-content: center;
    grid-auto-rows: 30em;
    width: 90%;
    margin: 0 auto;
  }
  &__card {
    border: 0.5em outset var(--secondary-color);
    box-shadow: 0 0 2.5em -1em hsla(212, 29%, 19%, 0.685);
    @for $i from 1 to 5 {
      &:nth-child(#{$i}) {
        @include fadeIn(calc(750ms * #{$i}));
      }
    }

    &__top {
      display: flex;
      height: 20em;
      position: relative;
    }
    &__bottom {
      @include flexWrap(space-around, center);
      height: 10em;
    }
  }
  &__image {
    height: 100%;
    width: 100%;
    object-fit: fill;
  }
  &__caption {
    position: absolute;
    bottom: 10%;
    left: 50%;
    transform: translateX(-50%);
    font-size: var(--md);
  }
}
</style>
