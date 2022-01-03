<template>
  <div class="carusel">
    <div
      class="carusel-wrapper"
      :style="{
        'margin-left': '-' + 100 * count + '%',
        transition: '0.9s',
      }"
    >
      <vCaruselItem
        v-for="item in carusel_data"
        :key="item.id"
        :caruselItem="item"
      />
    </div>
    <div class="btn">
      <button class="btn" @click="prev">prev</button>
      <button class="btn" @click="next">next</button>
    </div>
  </div>
</template>

<script>
import vCaruselItem from "./carulse-item.vue";
export default {
  name: "vCarusel",
  components: {
    vCaruselItem,
  },
  props: {
    carusel_data: {
      type: Array,
      default: null,
    },
    timerItem: {
      type: Number,
      default: null,
    },
  },
  data() {
    return {
      count: 0,
    };
  },
  methods: {
    next() {
      if (this.count >= this.carusel_data.length - 7) {
        this.count = 0;
      } else return this.count++;
    },
    prev() {
      this.count--;
    },
  },
  mounted() {
    if (this.timerItem > 0) {
      setInterval(() => {
        this.next();
      }, this.timerItem);
    }
  },
};
</script>

<style lang="scss">
.carusel {
  width: 450px;
  // border: 2px solid red;
}
.carusel-wrapper {
  display: flex;
}
</style>
