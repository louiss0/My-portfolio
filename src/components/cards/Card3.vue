 target="blank"<template>
  <div class="resume__card">
    <div class="resume__card__top">
      <img
        src="../../assets/img/Screenshot_2019-07-23 Fast Pizza.png"
        alt="mountains"
        class="resume__image"
      />
      <figcaption class="resume__caption">{{cards[2].caption}}</figcaption>
    </div>
    <div class="resume__card__bottom">
      <a :href="cards[2].code" target="blank">
        <svg class="icon icon--yellow">
          <use href="../../assets/social/spriteSmedia.svg#icon-github" />
        </svg>
      </a>
      <a :href="cards[2].site" target="blank">Website</a>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    cards: Array
  }
};
</script>

<style>
</style>
