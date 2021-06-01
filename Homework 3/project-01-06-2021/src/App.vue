<template>
  <div id="app">
    <product-card
      v-for="(item, index) in productList"
      :key="index"
      :image-src="item.imageSrc"
      :product-title="item.productTitle"
      :product-link="item.productLink"
      :product-price="item.productPrice"
      :is-in-store="item.isInStore"
    />
    <!-- <product-card
      image-src="https://content.rozetka.com.ua/goods/images/preview/11314684.jpg"
      product-title="Тример універсальний PHILIPS Series 5000"
      product-link="https://bt.rozetka.com.ua/ua/philips_mg5730_15/p24852941/"
      product-price="1599 грн"
    />
    <product-card
      imageSrc="https://content.rozetka.com.ua/goods/images/preview/101601326.png"
      productTitle="MSI PCI-Ex GeForce GTX 1660 Super Gaming X 6GB GDDR6 (192bit)
    (1830/14000) (HDMI, 3 x DisplayPort) (GTX 1660 SUPER GAMING X)"
      productLink="https://hard.rozetka.com.ua/ua/msi_gtx_1660_super_gaming_x/p143436890/"
      productPrice="8599 грн"
    /> -->
  </div>
</template>

<script>
import ProductCard from "./components/ProductCard.vue";

export default {
  name: "App",
  components: {
    ProductCard,
  },
  data() {
    return {
      productList: [
        {
          id: 1,
          imageSrc:
            "https://content.rozetka.com.ua/goods/images/preview/11314684.jpg",
          productTitle: "Тример універсальний PHILIPS Series 5000",
          productLink:
            "https://bt.rozetka.com.ua/ua/philips_mg5730_15/p24852941/",
          productPrice: "1599 грн",
          isInStore: false,
        },
        {
          id: 2,
          imageSrc:
            "https://content.rozetka.com.ua/goods/images/preview/101601326.png",
          productTitle:
            "MSI PCI-Ex GeForce GTX 1660 Super Gaming X 6GB GDDR6 (192bit) (1830/14000) (HDMI, 3 x DisplayPort) (GTX 1660 SUPER GAMING X)",
          productLink:
            "https://hard.rozetka.com.ua/ua/msi_gtx_1660_super_gaming_x/p143436890/",
          productPrice: "8599 грн",
          isInStore: true,
        },
      ],
    };
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
  align-items: flex-start;
}
</style>
