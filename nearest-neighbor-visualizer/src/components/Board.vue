<template>
    <div class="container">
        <div class="border-gray-700 border-4" v-for="gridElement in gridElements" :key="gridElement.id">
        </div>
    </div>
</template>

<script lang="ts">
import { ref } from 'vue';
import { Options, Vue, setup } from 'vue-class-component'
import { GridElement } from '../types/GridElement';

@Options({
    props: {
        width: {
            type: Number,
            default: 20
        },
        height: {
            type: Number,
            default: 20
        }
    }
})
export default class Board extends Vue {
    width!: Number;
    height!: Number;

    gridElements = setup(() => {
        const gridElements = ref<GridElement[]>([]);

        for (let i = 0; i < this.width; i++) {
            for (let j = 0; j < this.height; j++) {
                gridElements.value.push({ id: `${i}-${j}`})
            }
        }
        debugger

        return { gridElements };
    });

}
</script>

<style scoped></style>
