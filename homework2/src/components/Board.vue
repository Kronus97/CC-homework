<template>
  <div class="flex h-5/6 pt-8 justify-center content-center">
    <div class="flex flex-wrap w-full">
      <div
        class="flex shadow-strong"
        :style="{ width: `${width}%`, height: `${width}%` }"
        v-for="gridElement in gridElements"
        :key="gridElement.id"
      ></div>
    </div>
  </div>
</template>

<script lang="ts">
import { defineComponent, ref } from "vue";
import { GridElement } from "../types/GridElement";

export default defineComponent({
  name: "Board",
  props: {
    rows: {
      required: false,
      type: Number,
      default: 50,
    },
    columns: {
      required: false,
      type: Number,
      default: 50,
    },
  },
  setup(props) {
    const gridElements = ref<GridElement[]>([]);

    for (let i = 0; i < props.rows; i++) {
      for (let j = 0; j < props.columns; j++) {
        gridElements.value.push({ id: `${i}-${j}` });
      }
    }

    const width = 100 / props.columns;
    const height = 100 / props.rows;

    return { gridElements, width, height };
  },
});
</script>

<style></style>
