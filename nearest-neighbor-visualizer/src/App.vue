<template>
  <Nav/>
</template>

<script lang="ts">
import { Options, Vue } from "vue-class-component";
import Nav from "./components/Nav.vue";
import Grid from "./components/Grid.vue";

@Options({
  components: {
    Nav,
    Grid,
  },
})
export default class App extends Vue {}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}
</style>
