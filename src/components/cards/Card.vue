<template>
  <div class="resume__card">
    <div class="resume__card__top">
      <img
        src="../../assets/img/Screenshot_2019-08-11 Burger Builder.png"
        :alt="card1.caption"
        class="resume__image"
      />
      <figcaption class="resume__caption">{{card1.caption}}</figcaption>
    </div>
    <div class="resume__card__bottom">
      <a :href="card1.code" target="blank">
        <svg class="icon icon--yellow">
          <use href="../../assets/social/spriteSmedia.svg#icon-github" />
        </svg>
      </a>
      <a :href="card1.site" target="blank">Website</a>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    card1: Object
  }
};
</script>

<style>
</style>
