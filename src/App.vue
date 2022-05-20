<template>
  <div class="container">
    <products-list-view />
  </div>
</template>

<script>
import ProductsListView from './views/ProductsListView'

export default {
  name: 'App',
  components: {
    ProductsListView
  }
}
</script>

<style lang="scss">
@import url('https://fonts.googleapis.com/css2?family=Source+Sans+Pro:wght@400;600&display=swap');
@import url('https://fonts.googleapis.com/css2?family=Inter:wght@600&display=swap"');

* {
  box-sizing: border-box;
}

body {
  font-family: 'Source Sans Pro', sans-serif;
}

.container {
  max-width: 1440px;
  margin: auto;
  padding: 0 32px;

  @media screen and (max-width: 940px) {
    padding: 0 15px;
  }
}
</style>
