<template>
  <div class="options"
       @click="isActive = !isActive"
  >
    <div class="options__item options__item-default">По умолчанию</div>

    <div class="options__drop-down-list"
         :class="{ open: isActive }"
    >
      <div class="options__item">По заголовку</div>
      <div class="options__item">По цене</div>
    </div>
  </div>
</template>

<script>
export default {
  name: "Options",
  data() {
    return {
      isActive: false
    }
  }
}
</script>

<style lang="scss" scoped>
.options {
  background-color: #FFFEFB;
  box-shadow: 0 2px 5px rgba(0, 0, 0, 0.1);
  border-radius: 4px;
  padding: 10px 16px;
  width: 121px;
  height: 36px;
  z-index: 22;
  cursor: pointer;

  &__item {
    font-weight: 400;
    font-size: 12px;
    line-height: 15px;
    color: #3F3F3F;
    transition: 0.2s;

    &:hover {
      color: #B4B4B4;
    }
  }

  &__item-default {
    position: relative;
    color: #B4B4B4;

    &:after {
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
  }

  &__drop-down-list {
    position: absolute;
    bottom: 0;
    left: 0;
    background-color: #FFFEFB;
    box-shadow: 0 2px 5px rgba(0, 0, 0, 0.1);
    border-radius: 4px;
    padding: 5px 10px;
    width: 100%;
    opacity: 0;
    pointer-events: none;

    &.open {
      pointer-events: all;
      z-index: inherit;
      animation: slideDown 300ms 60ms ease-in-out forwards;
    }

    & .options__item {
      padding: 5px 0;
    }
  }
}

@keyframes slideDown {
  0% {
    opacity: 0;
    transform: translateY(98%);
  }

  50% {
    opacity: 0.5;
    transform: translateY(100%);
  }

  100% {
    opacity: 1;
    transform: translateY(calc(100% + 4px));
  }
}
</style>