<template>
    <div>
        <p v-if="esta_trabalhando">Estou trabalhando no momento</p>
        <p v-else>Estou desempregado</p>
        <p>Ele é um programador</p>
        <div>
        <p>E sabe as seguintes linguagens de backend:</p>
        <ul>
            <li v-for="(tecno, index) in back_tecno" :key="index">
                {{ tecno }}
            </li>
        </ul>
        <p>E sabe as seguintes linguagens de frontend:</p>
        <ul>
            <li v-for="tecno in front_tecno" :key="tecno.id">
                {{ tecno.language }}
            </li>
        </ul>
        </div>
        <div>
            <button @click="showEmail">{{ textButton }}</button>
        </div>
        <p v-show="mostrar_email">{{ email }}</p>
        <p>Open de google <a v-bind:href="meu_link" target="_blank">HERE</a></p>
        <Picture />
    </div>
</template>

<script>
import Picture from './Picture.vue'

export default {
    name: 'Info',
    components: {
        Picture
    },
    props: {
        email: String
    },
    data() {
        return {
            esta_trabalhando: false,
            mostrar_email: false,
            meu_link: 'https://google.com',
            textButton: 'Mostrar email',
            back_tecno: ['Java', 'Node', 'C#'],
            front_tecno: [
                {id: 1, language: 'HTML'},
                {id: 2, language: 'CSS'},
                {id: 3, language: 'JS'}
            ]
        }
    },
    methods: {
        showEmail() {
            this.mostrar_email = !this.mostrar_email
            if(!this.mostrar_email){
                this.textButton = 'Mostrar email'
            }else{
                this.textButton = 'Esconder email'
            }
        }
    }
}
</script>
