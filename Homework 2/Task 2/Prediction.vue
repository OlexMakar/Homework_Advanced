<template>
  <div>
    <div>
      <button @click="getPrediction">Отримати передбачення!</button>
    </div>
    <div>
      <span>
        {{ yourPrediction }}
      </span>
    </div>
  </div>
</template>
<script>
export default {
  name: "prediction",
  data() {
    return {
      yourPrediction: null,
      predictionArray: [
        "Удача прийде звідки не чекаєте.",
        "Всі незакінчені справи будуть завершені.",
        "Яскрава пригода вже чекає вас.",
        "Вас чекає несподіване грошове надходження.",
      ],
    };
  },
  methods: {
    getRandom(min, max) {
      return min + Math.floor(Math.random() * (max - min + 1));
    },
    getPrediction() {
      const randIndex = this.getRandom(0, this.predictionArr.length - 1);
      this.yourPrediction = this.predictionArr[randIndex];
    },
  },
};
</script>
<style lang="scss" scoped></style>