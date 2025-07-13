<template>
  <header>
    <img alt="Vue logo" class="logo" src="./assets/logo.svg" width="125" height="125" />

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
  </header>

  <main>
    <TheWelcome />
  </main>
</template>

<script>
import TheWelcome from './components/TheWelcome.vue'

export default {
  name: 'App',
  components: {
    TheWelcome
  },
  data() {
    return {
      스타일 : 'color:red',
      price1: 60,
      price2: 70,
      price3: 80,
      products: ['역삼동원룸', '천호동원룸', '마포구원룸']
    }
  }
}
</script>

<style scoped>
header {
  line-height: 1.5;
}

.logo {
  display: block;
  margin: 0 auto 2rem;
}

@media (min-width: 1024px) {
  header {
    display: flex;
    place-items: center;
    padding-right: calc(var(--section-gap) / 2);
  }

  .logo {
    margin: 0 2rem 0 0;
  }

  header .wrapper {
    display: flex;
    place-items: flex-start;
    flex-wrap: wrap;
  }
}
</style>
