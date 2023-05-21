<template >
  <section class="appSection">
    <NavBar :title="title"/>
    <p> {{ sumNumber }}</p>
    <div :class="{red: changeColor}">Change my color</div>
    <buton @click="onClick">Click me!</buton>
    <AppFooter :name="name"/>
  </section>
  </template>
  
  <script>
  import NavBar from './components/NavBar.vue';
  import AppFooter from './components/AppFooter.vue';
  export default {
    name: 'App',
    components: {
      NavBar,
      AppFooter
    },
    data() {
      return {
        title: "Hello",
        name: "Goodbye",
        number: 10,
        changeColor: false
      }
    },
    computed: {
      sumNumber() {
        return this.number + 2
      }
    },
    methods: {
      onClick() {
        this.changeColor = !this.changeColor
      }
    }
  }
  </script>
  
  <style scoped>
  .appSection {
    display: flex;
    justify-content: center;
    flex-direction: column;
    align-items: center;
  }
  
  .red {
    background-color: red;
  }
  </style>
  