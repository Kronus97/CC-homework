<template>
  <div>

  </div>
</template>

<script lang="ts">
import { Options, Vue } from "vue-class-component";
import { GridElement } from "../types/GridElement";


@Options({
    props: {
        cell: {
            type: GridElement,
            default: null
        }
    }
})
export default class Cell extends Vue {

}
</script>