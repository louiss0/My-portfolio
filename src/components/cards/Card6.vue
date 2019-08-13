<template>
  <div class="resume__card">
    <div class="resume__card__top">
      <img
        src="../../assets/img/Screenshot_2019-08-10 Budget Builder.png"
        alt="mountains"
        class="resume__image"
      />
      <figcaption class="resume__caption">{{card6.caption}}</figcaption>
    </div>
    <div class="resume__card__bottom">
      <a :href="card6.code" target="blank">
        <svg class="icon icon--yellow">
          <use href="../../assets/social/spriteSmedia.svg#icon-github" />
        </svg>
      </a>
      <a :href="card6.site" target="blank">Website</a>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    card6: Object
  }
};
</script>

<style>
</style>
