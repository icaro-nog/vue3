<template>
    <div>
        <button @click="primeiro(txt1, $events), segundo(txt2, $events), terceiro(txt3, $events)">Ativar multiplos Eventos</button>
        <p>{{ multiplos_eventos }}</p>
    </div>
</template>

<script>
    export default {
        name: 'MultiplosEventos',
        data() {
            return {
                multiplos_eventos: '',
                txt1: 'Primeiro evento',
                txt2: 'Segundo evento',
                txt3: ''
            }
        },
        methods: {
            primeiro(txt, e) {
                this.multiplos_eventos = txt
            },
            segundo(txt, e) {
                setTimeout(() => this.multiplos_eventos = txt, 500)
            },
            terceiro(txt, e) {
                setTimeout(() => this.multiplos_eventos = txt, 1000)
            }
        }
    }
</script>

<style scoped>
    div {
        margin: 100px;
    }
</style>