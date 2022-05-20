<template>
  <div class="options">
    <div class="options__item options__item-default">По умолчанию</div>

    <div class="options__list-item">
      <div class="options__item">По заголовку</div>
      <div class="options__item">По цене</div>
    </div>
  </div>
</template>

<script>
export default {
  name: "Options"
}
</script>

<style lang="scss" scoped>
.options {
  position: relative;
  background-color: #FFFEFB;
  box-shadow: 0 2px 5px rgba(0, 0, 0, 0.1);
  border-radius: 4px;
  padding: 10px 16px;
  width: 121px;
  height: 36px;
  z-index: 22;
  cursor: pointer;
}

.options__item {
  font-weight: 400;
  font-size: 12px;
  line-height: 15px;
  color: #3F3F3F;
  transition: 0.2s;
}

.options__item:hover {
  color: #B4B4B4;
}

.options__item-default {
  position: relative;
  color: #B4B4B4;
}

.options__item-default:after {
  position: absolute;
  content: '';
  width: 8px;
  height: 6px;
  right: -6px;
  top: 50%;
  transform: translateY(-50%);
  background-image: url("../assets/arrow-bottom.svg");
  background-position: center;
  background-repeat: no-repeat;
  background-size: contain;
}

.options__list-item {
  position: absolute;
  bottom: 0;
  left: 0;
  background-color: #FFFEFB;
  box-shadow: 0 2px 5px rgba(0, 0, 0, 0.1);
  border-radius: 4px;
  padding: 5px 10px;
  width: 100%;
  transform: translateY(calc(100% + 2px));
  opacity: 0;
  pointer-events: none;
  z-index: -1;
}

.options__list-item .options__item {
  padding: 5px 0;
}

.options__list-item_open {
  opacity: 1;
  pointer-events: all;
  z-index: 1;
}


</style>