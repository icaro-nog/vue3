<template>
    <div>
        <img :src="avatar" :alt="descricao">
        <p>aqui</p>
        <Reutilizacao />
        <p>aqui</p>
        <p>aqui</p>
        <p>aqui</p>
        <p>aqui</p>
    </div>
</template>

<script>
    import Reutilizacao from './Reutilizacao.vue'

    export default {
        name: 'Picture',
        data() {
            return {
                avatar: '/img/avatar.png',
                descricao: 'Ícaro'
            }
        },
        components: {
            Reutilizacao
        }
    }
</script>