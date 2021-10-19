<template>
    <div class="w-screen h-12 bg-gray-500"></div>
</template>

<script lang="ts">
import { Options, Vue } from 'vue-class-component'

@Options({
    props: {
        msg: String,
    },
})
export default class Nav extends Vue {
    msg!: string
}
</script>

<style scoped></style>
