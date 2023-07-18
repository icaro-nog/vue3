<template>
    <div>
        <p v-if='esta_trabalhando'>Estou trabalhando no momento.</p>
        <p v-else>Estou em busca de novas oportunidades!</p>
        <p>Utilizo as seguintes tecnologias:</p>
        <ul>
            <li>JavaScript</li>
            <li>PHP</li>
            <li>Python</li>
        </ul>
        <p v-show="mostrar_email">Mande uma mensagem para: {{ email }}</p>
        <p>Acesse meu portfolio neste link: <a v-bind:href="meu_link" target="_blank">link</a> </p>
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
                mostrar_email: true,
                email: 'icaro@teste.com.br',
                meu_link: 'https://www.google.com.br'
            }
        }
    }
</script>