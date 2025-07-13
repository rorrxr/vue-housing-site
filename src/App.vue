<template>
  <div class="menu">
    <a v-for="m in menuItem" :key="m">{{ m }}</a>
  </div>
  <div>
    <h4 :style="스타일">{{ products[0] }}</h4>
    <p>{{ price1 }}만원</p>
  </div>
  <div>
    <h4>{{ products[1] }}</h4>
    <p>{{ price2 }}만원</p>
  </div>
  <div>
    <h4>{{ products[2] }}</h4>
    <p>{{ price3 }}만원</p>
  </div>
</template>

<script>
export default {
  name: 'App',
  data() {
    return {
      스타일: 'color:red',
      menuItem: ['Home', 'Shop', 'About'],
      price1: 60,
      price2: 70,
      price3: 80,
      products: ['역삼동원룸', '천호동원룸', '마포구원룸']
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
