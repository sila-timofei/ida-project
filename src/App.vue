<template>
  <products-list-view />
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
@import url('https://fonts.googleapis.com/css2?family=Inter:wght@600&display=swap" rel="stylesheet');

* {
  box-sizing: border-box;
}

body {
  font-family: 'Source Sans Pro', sans-serif;
}
</style>
