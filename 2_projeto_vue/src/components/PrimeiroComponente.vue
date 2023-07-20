<template>
  <div>
    <h1>Olá Vue!</h1>
    <MultiplosEventos />
  </div>
</template>

<script>
  import MultiplosEventos from './MultiplosEventos.vue';

  export default {
    name: 'PrimeiroComponente',
    components: {
      MultiplosEventos
    }
  }
</script>