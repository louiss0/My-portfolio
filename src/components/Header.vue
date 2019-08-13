<template>
  <header class="resume--header">
    <h1 class="text--lg">{{name}}</h1>
    <div class="resume--header__info">
      <h2>{{line}}</h2>
      <h3 class="text--sm">{{setMonth()}}/{{day}}/{{year}}</h3>
    </div>
  </header>
</template>

<script>
const date = new Date();
const month = date.getMonth() + 1;
const day = date.getDate();
const year = date.getFullYear();
export default {
  data() {
    return {
      name: "Shelton louis",
  line: "These are the projects that im proud of",
      day,
      month,
      year
    };
  },
  methods: {
    setMonth() {
      if (this.month > 12) {
        this.month = 1;
      }
      return this.month;
    }
  }
};
</script>

<style lang='scss'>
@import "../scss/abstracts.scss";
.resume--header {
  @include flexCenter(space-around, center);
  @include fadeIn(500ms);
  &__info {
    width: 60%;
    @include flexWrap(space-evenly, center);

    .text--sm {
      margin: 1em;
      @for $i from 1 through 3 {
        &:nth-child(#{$i}) {
          @include fadeIn(calc(500ms * #{$i}));
        }
      }
    }
  }
}
</style>
