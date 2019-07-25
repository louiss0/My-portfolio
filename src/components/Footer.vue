<template>
  <footer class="resume--footer">
    <h1 class="text--md">Skills</h1>
    <h2 class="text--sm">
      <a class="resume--footer__link" :href="url" target="blank">Click Here</a>
      for More projects
    </h2>
    <div class="resume--footer__grid">
      <div class="resume--footer__grid__item">HTML</div>
      <div class="resume--footer__grid__item">
        <svg class="icon">
          <use href="../assets/framework/SVG/sprite.svg#icon-sass" />
        </svg>SCSS
      </div>
      <div class="resume--footer__grid__item">
        <svg class="icon">
          <use href="../assets/framework/SVG/sprite.svg#icon-react" />
        </svg> React
      </div>
      <div class="resume--footer__grid__item">
        <svg class="icon">
          <use href="../assets/framework/SVG/sprite.svg#icon-vue-dot-js" />
        </svg>Vue
      </div>
    </div>
  </footer>
</template>

<script>
export default {
  data() {
    return {
      url: "https://app.netlify.com/teams/louiss0/sites"
    };
  }
};
</script>

<style lang="scss">
@import "../scss/abstracts.scss";
.resume--footer {
  @include flexCenter(space-evenly, center);
  &__grid {
    width: 80%;
    display: grid;
    grid-template-columns: repeat(auto-fill, 15em);
    grid-column-gap: 5em;
    grid-gap: 2em;
    &__item {
      font-size: var(--sm);
      @include flexWrap(space-around, center);
    }
  }
  &__link {
    color: var(--mid-blue);
  }
}
</style>
