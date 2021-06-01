<template>
  <div class="container">
    <div class="image">
      <a :href="productLink">
        <img :src="imageSrc" alt="product" />
      </a>
    </div>
    <div>
      <a :href="productLink">{{ productTitle }}</a>
    </div>
    <div>
      {{ productPrice }}
    </div>
    <div>
      {{ isAvailable }}
    </div>
  </div>
</template>

<script>
export default {
  name: "ProductCard",
  //Дані, необхідні для створення компонента:
  props: {
    imageSrc: {
      type: String,
      default: "https://bytes.ua/wp-content/uploads/2017/08/no-image.png",
    },
    productTitle: {
      type: String,
      default: "no title",
    },
    productLink: {
      type: String,
      default: "https://rozetka.com.ua/ua/",
    },
    productPrice: {
      type: [Number, String],
      default: 0,
    },
    isInStore: {
      type: Boolean,
      default: true,
    },
  },
  computed: {
    isAvailable() {
      return this.isInStore ? "У наявності" : "Немає у наявності";
    },
  },
};
</script>

<style lang="css" scoped>
.container {
  color: black;
  display: inline-block;
  height: 300px;
  width: 150px;
  border: 2px solid blue;
  border-radius: 5px;
}
</style>