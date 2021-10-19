<template>
    <div>
        <Nav />
        <Board :height="20" :width="20" />
    </div>
</template>

<script lang="ts">
import { Options, Vue } from 'vue-class-component'
import Nav from './components/Nav.vue'
import Board from './components/Board.vue'

@Options({
    components: {
        Nav,
        Board,
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
