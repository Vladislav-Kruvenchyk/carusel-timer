<template>
  <div class="carusel-item">
    <img :src="require('../../assets/images/' + caruselItem.image)" alt="" />
  </div>
</template>

<script>
export default {
  name: "vCaruselItem",
  props: {
    caruselItem: {
      type: [Object, Array],
      default: null,
    },
  },
};
</script>

<style lang="scss">
img {
  width: 150px;
  height: 150px;
}
</style>
