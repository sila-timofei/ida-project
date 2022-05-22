<template>
  <form class="form">
    <div class="form__field-label">Наименование товара</div>
    <input type="text" class="form__field" placeholder="Введите наименование товара">

    <div class="form__field-label form__label-not-necessary">Описание товара</div>
    <textarea class="form__field form__big-field" id="" placeholder="Введите описание товара"></textarea>

    <div class="form__field-label">Ссылка на изображение товара</div>
    <input type="text" class="form__field" placeholder="Введите ссылку">

    <div class="form__field-label">Цена товара</div>
    <input type="text" class="form__field" placeholder="Введите цену">

    <button type="button" class="form__btn-send form__btn-send_active">Добавить товар</button>
  </form>
</template>

<script>
export default {
  name: "AddProductForm"
}
</script>

<style lang="scss" scoped>
.form {
  position: sticky;
  top: 24px;
  padding: 24px;
  background: #FFFEFB;
  box-shadow: 0 20px 30px rgba(0, 0, 0, 0.04), 0 6px 10px rgba(0, 0, 0, 0.02);
  border-radius: 4px;
  min-width: 332px;
  display: flex;
  flex-direction: column;

  @media screen and (max-width: 640px) {
    min-width: 50%;
    padding: 16px;
  }

  @media screen and (max-width: 560px) {
    min-width: 100%;
    position: static;
    margin-bottom: 68px;
  }
}

.form__field {
  margin-bottom: 16px;
  background: #FFFEFB;
  box-shadow: 0 2px 5px rgba(0, 0, 0, 0.1);
  border-radius: 4px;
  padding: 10px 16px;
  outline: none;
  border: 1px solid transparent;
  transition: 0.4s;
}

.form__field:focus {
  box-shadow: 0 2px 10px rgba(23, 118, 227, 0.26);
}

.form__big-field {
  height: 108px;
  width: 100%;
  max-width: 100%;
  font-family: "Arial", sans-serif;
}

.form__field_error {
  border: 1px solid #FF8484;
}

.form__field-label {
  position: relative;
  font-style: normal;
  font-weight: 400;
  font-size: 10px;
  line-height: 13px;
  letter-spacing: -0.02em;
  color: #49485E;
  margin-bottom: 4px;
  align-self: flex-start;
}

.form__field-label:after {
  position: absolute;
  content: '';
  right: -5px;
  top: 0;
  width: 4px;
  height: 4px;
  border-radius: 50%;
  background-color: #FF8484;
}

.form__label-not-necessary:after {
  display: none;
}

.form__btn-send {
  background-color: #EEEEEE;
  box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
  padding: 10px 16px;
  border-radius: 10px;
  font-family: 'Inter', sans-serif;
  font-weight: 600;
  font-size: 12px;
  line-height: 15px;
  color: #B4B4B4;
  border: none;
  cursor: not-allowed;
  margin-top: 14px;
  transition: 0.2s;
}

.form__btn-send_active {
  background-color: #7BAE73;
  color: #FFFFFF;
  cursor: pointer;
}

.form__btn-send_active:hover {
  background-color: #5ca84b;
}

.form__btn-send_active:focus:not(:active) {
  box-shadow: 0 0 0 0.125em rgb(92, 168, 75);
}

.form__btn-send_active:focus {
  border-color: transparent;
  color: #fff;
}
</style>