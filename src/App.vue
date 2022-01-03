<template>
  <div class="app">
    <vCarusel :carusel_data="caruselData" :timerItem="2000" />
  </div>
</template>

<script>
import vCarusel from "./components/carusel/carusel.vue";
export default {
  name: "app",
  components: {
    vCarusel,
  },
  data: () => {
    return {
      caruselData: [
        { id: 1, image: "1.png" },
        { id: 2, image: "2.png" },
        { id: 3, image: "3.png" },
        { id: 4, image: "4.png" },
        { id: 5, image: "5.png" },
        { id: 6, image: "6.png" },
        { id: 7, image: "7.png" },
        { id: 8, image: "8.png" },
        { id: 9, image: "9.png" },
        // { id: 10, image: "10.png" },
      ],
    };
  },
};
</script>

<style lang="scss">
.app {
  width: 450px;
  overflow: hidden;
  margin: 0 auto;
}
.btn {
  padding: 10px;
  cursor: pointer;
  margin: 2px;
}
</style>
