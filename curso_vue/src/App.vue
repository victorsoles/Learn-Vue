<template>
  <div>
  <FirstComponent />
  <p>Meu Jogo favorito é {{ test }}</p>
  </div>
</template>

<script>
import FirstComponent from './components/FirstComponent.vue'

  export default {
  components: { FirstComponent },
    name: 'App',
    Components: {
      FirstComponent
    },
    data() {
      return {
        test: "Among Us"
      }
    }
  }
</script>
