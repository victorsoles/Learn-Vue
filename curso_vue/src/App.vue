<template>
  <div>
  <Header />
  <FirstComponent />
  <p>Meu Jogo favorito é {{ test }}</p>
  <LifeCycle />
  <Person />
  <Info />
  </div>
</template>

<script>
  import Header from './components/Header.vue'
  import Info from './components/Info.vue'
  import FirstComponent from './components/FirstComponent.vue'
  import LifeCycle from './components/LifeCycle.vue'
  import Person from './components/Person.vue'

  export default {
    name: 'App',
    components: {
      Header,
      FirstComponent,
      LifeCycle,
      Person,
      Info
    },
    data() {
      return {
        test: "Among Us"
      }
    }
  }
</script>

<style>
  body{
    background-color: rgb(14, 13, 14);
    color: #dbe2db;
  }
</style>