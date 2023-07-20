<template>
  <div>
    <h1>Olá Vue!</h1>
    <MultiplosEventos />
    <Reutilizacao />
    <Reutilizacao />
    <Reutilizacao />
    <Reutilizacao />
  </div>
</template>

<script>
  import MultiplosEventos from './MultiplosEventos.vue';
  import Reutilizacao from './Reutilizacao.vue';

  export default {
    name: 'PrimeiroComponente',
    components: {
      MultiplosEventos,
      Reutilizacao
    }
  }
</script>