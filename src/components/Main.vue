<template lang="pug" > 
  main.resume--main
    <card :card1='cards[0]'/>
    <card2 :card2='cards[1]'/>
    <card3 :card3='cards[2]'/>
    <card4 :card4='cards[3]'/>
    <card5 :card5='cards[4]'/>
    <card6 :card6='cards[5]'/>
      
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
          caption: "Burger Builder",
          code: "https://github.com/louiss0/burger-builder",
          site: "https://burgerbuilderap.netlify.com"
        },
        {
          caption: "Stock Trader",
          code: "https://github.com/louiss0/stock-trader",
          site: "https://stocktrade.netlify.com"
        },
        {
          caption: "Pixabay",
          code: "https://github.com/louiss0/pixabay",
          site: "https://pixabay-site.netlify.com"
        },
        {
          caption: "Monster Slayer",
          code: "https://github.com/louiss0/monster-slayer",
          site: "https://monster-slayer.netlify.com"
        },
        {
          caption: "Users",
          code: "https://github.com/louiss0/users",
          site: "https://fiveusers.netlify.com"
        },
        {
          caption: "Expense App",
          code: "https://github.com/louiss0/budget-builder",
          site: "https://expensebudgeter.netlify.com"
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
