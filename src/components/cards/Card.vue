<template functional>
  <figure class="resume__card">
    <slot name="card-slot" :singleCard="props.card" ></slot>
  </figure>
</template>

<script>
export default {
  props: {
    card: Object
  }
};
</script>
<style>
</style>
