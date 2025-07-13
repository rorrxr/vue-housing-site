<template>
  <div class="menu">
    <a v-for="m in menuItem" :key="m">{{ m }}</a>
  </div>

  <div>
    <a v-for="m in productItem" :key="m">{{ m }}</a>
    <a v-for="m in priceItem" :key="m">{{ m }}</a>
  </div>


</template>

<script>
export default {
  name: 'App',
  data() {
    return {
      menuItem: ['Home', 'Shop', 'About'],
      priceItem : [60, 70, 80],
      productItem: ['역삼동원룸', '천호동원룸', '마포구원룸']
    }
  }
}
</script>

<style scoped>
.logo {
  display: block;
  margin: 0 auto 2rem;
}

.menu {
  background: darkslateblue;
  padding: 15px;
  border-radius: 5px;
}

.menu a {
  color: white;
  padding: 10px;
}

</style>
