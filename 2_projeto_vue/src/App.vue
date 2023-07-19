<template>
    <div>
      <Header />
      <PrimeiroComponente />
      <Info />
    </div>
</template>

<script>
import PrimeiroComponente from './components/PrimeiroComponente.vue'
import Info from './components/Info.vue';
import Header from './components/Header.vue';

export default {
  name: 'App',
  components: {
    PrimeiroComponente,
    Info,
    Header
  }
}
</script>

<style>
  body {
    background-color: #333;
    color: #fff;
  }

  a {
    color: red;
  }

  .paragrafo_email {
    background-color: green;
  }
</style>