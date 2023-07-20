<template>
    <div>
        <h2>Meu formulário:</h2>
        <form action="" @submit.prevent="enviar_formulario">
            <div>
                <input type="text" v-model="name">
            </div>
            <div>
                <input type="text" v-model="email">
            </div>
            <div>
                <Submit />
            </div>
        </form>
    </div>
</template>

<script>
    import InputText from './Form/InputText.vue';
    import Submit from './Form/Submit.vue';

    export default {
        name: 'Form',
        components: {
            InputText,
            Submit
        },
        data(){
            return {
                name: '',
                email: ''
            }
        },
        methods: {
            enviar_formulario() {

                const name = this.name;
                const email = this.email;

                console.log('form enviadoooo')
                console.log("O nome é: " + name)
                console.log("O email é: " + email)
            }
        }
    }
</script>