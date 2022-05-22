<template>
  <div class="product-card">
    <div class="product-card__btn-delete"></div>

    <div class="product-card__wrap-img">
      <img class="product-card__img" src="../assets/product.png" alt="">
    </div>

    <div class="product-card__info">
      <h4 class="product-card__name">Наименование товара</h4>
      <p class="product-card__descr">Довольно-таки интересное описание товара в несколько строк.
        Довольно-таки интересное описание товара в несколько строк</p>
      <div class="product-card__price">10 000 руб.</div>
    </div>
  </div>
</template>

<script>
export default {
  name: "CardProduct"
}
</script>

<style lang="scss" scoped>
.product-card {
  position: relative;
  width: 332px;
  background: #FFFEFB;
  box-shadow: 0 20px 30px rgba(0, 0, 0, 0.04), 0 6px 10px rgba(0, 0, 0, 0.02);
  border-radius: 4px;
  margin-bottom: 16px;
}

.product-card__wrap-img {
  height: 200px;
  overflow: hidden;
  border-radius: 4px 4px 0 0;
}

.product-card__img {
  width: 100%;
}

.product-card__info {
  padding: 16px 16px 24px;
}

.product-card__name {
  margin: 0 0 16px 0;
  font-weight: 600;
  font-size: 20px;
  line-height: 25px;
  color: #3F3F3F;
}

.product-card__descr {
  font-weight: 400;
  line-height: 20px;
  color: #3F3F3F;
  margin: 0 0 32px 0;
}

.product-card__price {
  font-weight: 600;
  font-size: 24px;
  line-height: 30px;
  color: #3F3F3F;
}

.product-card__btn-delete {
  position: absolute;
  right: -8px;
  top: -8px;
  width: 32px;
  height: 32px;
  background-color: #FF8484;
  box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
  border-radius: 10px;
  cursor: pointer;
  background-image: url("../assets/basket.svg");
  background-position: center;
  background-repeat: no-repeat;
  opacity: 0;
  transition: 0.2s;

  @media screen and (max-width: 940px) {
    opacity: 1;
  }
}

.product-card__btn-delete:hover {
  background-color: #ff6464;
}

.product-card:hover .product-card__btn-delete {
  opacity: 1;
}
</style>