<template>
    <div>
        <h2>Esta é a descrição de: {{ nome }}</h2>
        <Info :email="email" />
        <Info />
    </div>
</template>

<script>
import Info from './Info.vue'

export default {
    name: 'Person',
    components: {
        Info
    },
    data() {
        return {
            nome: "Vitin",
            email: "smurfet@rr.bot"
        }
    }
}
</script>
