<template>
    <h1>Qual o tamanho da sua casa: {{ casa }}</h1>
</template>

<script>
export default {
    name: 'LifeCycle',
    data() {
        return{
            casa: 'grande'
        }
    },
    created() {
        setTimeout(() => {
            this.casa = 'pequena'
        }, 1000);
    },
    mounted() {
        setTimeout(() => {
            this.casa = 'gigante'
        }, 2000);
    }
}
</script>
