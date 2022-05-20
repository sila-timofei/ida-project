<template>
  <div class="container">
    <div class="products-list-view__head">
      <h1 class="form__title">Добавление товара</h1>

    </div>

    <div class="products-list-view__content">
      <add-product-form class="products-list-view__form" />

      <div class="products-list-view__container-list">
        <products-list class="products-list-view__list" />
        <options class="products-list-view__options" />
      </div>
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

<style scoped>
.container {
  max-width: 1440px;
  margin: auto;
  padding: 0 32px;
}

.products-list-view__head {
  display: flex;
  margin: 32px 0 16px 0;
  align-items: center;
  justify-content: space-between;
}

.products-list-view__content {
  display: flex;
  align-items: flex-start;
}

.form__title {
  font-style: normal;
  font-weight: 600;
  font-size: 28px;
  line-height: 35px;
  color: #3F3F3F;
  margin: 0;
}

.products-list-view__container-list {
  position: relative;
}

.products-list-view__options {
  position: absolute;
  right: 0;
  top: -52px;
}

@media screen and (max-width: 940px) {
  .container {
    padding: 0 15px;
  }
}

@media screen and (max-width: 640px) {
  .products-list-view__form {
    min-width: 50%;
  }

  .products-list-view__container-list {
    width: 50%;
  }
}

@media screen and (max-width: 560px) {
  .products-list-view__content {
    flex-direction: column;
  }

  .products-list-view__form {
    min-width: 100%;
    position: static;
    margin-bottom: 68px;
  }

  .products-list-view__container-list {
    width: 100%;
  }

  .products-list-view__options {
    left: 0;
  }
}

</style>