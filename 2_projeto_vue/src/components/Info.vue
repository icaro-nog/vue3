<template>
    <div>
        <p v-if='esta_trabalhando'>Estou trabalhando no momento.</p>
        <p v-else>Estou em busca de novas oportunidades!</p>
        <p>Utilizo as seguintes tecnologias para backend:</p>
        <ul>
            <li v-for="(technology, index) in backend_technologies" v-bind:key="index" >{{ technology }}</li>
        </ul>
        <p>Utilizo as seguintes tecnologias para front-end</p>
        <ul>
            <li v-for="technology in frontend_technologies" :key="technology.id">{{ technology.language }}</li>
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
                backend_technologies: ['JavaScript', 'PHP', 'Python'],
                frontend_technologies: [
                    {id: 1, language: 'HTML'},
                    {id: 2, language: 'CSS'},
                    {id: 3, language: ' Vue'},
                ]
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