<template>
    <div>
        <h1>Olá Alexandro Marrone</h1>
        <p>Meu nome é {{ nome }} e sou {{ profissao }}</p>
    </div>
</template>

<script>
    export default {
        name:'FirstComponent',
        data() {
            return {
                nome: "Vitin Soles",
                profissao: "Astronauta"
            }
        }
    }
</script>
