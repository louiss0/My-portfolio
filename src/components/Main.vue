<template lang="pug" > 
  main.resume--main
    <card v-for='(card , index) of cards'  :card='card':key=' Math.random() + index' >
    <template #card-slot='{singleCard:{site, img ,caption, code}}'  >
      <div class="resume__card__top">
          <a :href="site" target="blank">
          <img :src="img" :alt="caption" class="resume__image" />
          <figcaption class="resume__caption">{{caption}}</figcaption>
      </a>
    </div>
    <div class="resume__card__bottom">
      <a href='code' target="blank">
        <svg class="icon icon--yellow">
          <use href="../assets/social/spriteSmedia.svg#icon-github" />
        </svg>
      </a>
      <a :href="site" target="blank">Website</a>
    </div>
     
    </template>
    </card>
</template>

<script>
import Card from "./cards/Card.vue";
export default {
  data() {
    return {
      cards: [
        {
          caption: "Burger Builder",
          code: "https://github.com/louiss0/burger-builder",
          site: "https://burgerbuilderap.netlify.com",
          img: "/img/Screenshot_2019-08-11 Burger Builder.png"
        },
        {
          caption: "Movie Search App",
          code: "https://github.com/louiss0/movie-app",
          site: "https://moviesearchappex.netlify.com",
          img: "/img/Screenshot_2019-09-24 movie-search.png"
        },
        {
          caption: "Beach Resort",
          code: "https://github.com/louiss0/beach-resort",
          site: "https://luxuirous.netlify.com/",
          img: "/img/Screenshot_2019-09-24 Luxurious Rooms.png"
        },
        {
          caption: "Ecommerce Project",
          code: "https://github.com/louiss0/ecom",
          site: "https://ecom0.netlify.com",
          img: "/img/Screen Shot 2019-09-24 at 17.36.57.png"
        }
      ]
    };
  },
  components: {
    card: Card
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
