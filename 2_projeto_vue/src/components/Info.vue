<template>
    <div>
        <p v-if='esta_trabalhando'>Estou trabalhando no momento.</p>
        <p v-else>Estou em busca de novas oportunidades!</p>
        <p>Utilizo as seguintes tecnologias para backend:</p>
        <ul v-for="technology in backend_technologies">
            <li>{{ technology }}</li>
        </ul>
        <div>
            <button @click="showEmail">{{ texto_botao }}</button>
        </div>
        <p v-show="mostrar_email">Mande uma mensagem para: {{ email }}</p>
        <p class="paragrafo_email">Acesse meu portfolio neste link: <a v-bind:href="meu_link" target="_blank">link</a> </p>
        <Picture />
    </div>
</template>
<script>
    import Picture from './Picture.vue';

    export default {
        name: 'Info',
        components: {
            Picture
        },
        data() {
            return { 
                esta_trabalhando: false,
                mostrar_email: false,
                email: 'icaro@teste.com.br',
                meu_link: 'https://www.google.com.br',
                texto_botao: 'Mostrar e-mail',
                backend_technologies: ['JavaScript', 'PHP', 'Python']
            }
        },
        methods: {
            showEmail(){
                this.mostrar_email = !this.mostrar_email
                if(!this.mostrar_email){
                    this.texto_botao = 'Mostrar e-mail'
                } else {
                    this.texto_botao = 'Esconder e-mail'
                }
            }
        }
    }
</script>