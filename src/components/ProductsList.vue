<template>
  <div class="products-list">
    <product-card
        class="product-list__card"
    />
    <product-card
        class="product-list__card"
    />
    <product-card
        class="product-list__card"
    />
    <product-card
        class="product-list__card"
    />
    <product-card
        class="product-list__card"
    />
    <product-card
        class="product-list__card"
    />
  </div>
</template>

<script>
import ProductCard from "./ProductCard"

export default {
  name: "ProductsList",
  components: {
    ProductCard
  }
}
</script>

<style lang="scss" scoped>
.products-list {
  display: flex;
  flex-wrap: wrap;
  margin-bottom: -16px;
}

.product-list__card {
  margin-left: 16px;
}

@media screen and (max-width: 1460px) {
  .product-list__card {
    width: 31.3333333%;
    margin-left: 2%;
  }
}

@media screen and (max-width: 1200px) {
  .product-list__card {
    width: 48%;
  }
}

@media screen and (max-width: 940px) {
  .product-list__card {
    width: 96%;
    margin-left: 4%;
  }
}

@media screen and (max-width: 560px) {
  .product-list__card {
    margin-left: 0;
    width: 100%;
  }
}
</style>