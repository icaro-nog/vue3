<template>
    <div>
      <PrimeiroComponente />
      <Info />
    </div>
</template>

<script>
import PrimeiroComponente from './components/PrimeiroComponente.vue'
import Info from './components/Info.vue';

export default {
  name: 'App',
  components: {
    PrimeiroComponente,
    Info
  }
}
</script>