<template>
  <h1 class="products-list-view__title">Добавление товара</h1>

  <div class="products-list-view">
    <add-product-form />

    <div class="products-list-view__container-list">
      <products-list />
      <options class="products-list-view__options" />
    </div>
  </div>
</template>

<script>
import ProductsList from "../components/ProductsList";
import AddProductForm from "../components/AddProductForm";
import Options from "../components/Options";

export default {
  name: "ProductsListView",
  components: {
    ProductsList, AddProductForm, Options
  }
}
</script>

<style lang="scss" scoped>
.products-list-view__title {
  font-style: normal;
  font-weight: 600;
  font-size: 28px;
  line-height: 35px;
  color: #3F3F3F;
  margin: 32px 0 16px 0;
}

.products-list-view {
  display: flex;
  align-items: flex-start;

  @media screen and (max-width: 560px) {
    flex-direction: column;
  }

  &__container-list {
    position: relative;

    @media screen and (max-width: 640px) {
      width: 50%;
    }

    @media screen and (max-width: 560px) {
      width: 100%;
    }
  }

  &__options {
    position: absolute;
    right: 0;
    top: -52px;

    @media screen and (max-width: 560px) {
      left: 0;
    }
  }
}
</style>