<script setup lang="ts">
import {JsonViewer} from "vue3-json-viewer";
import "vue3-json-viewer/dist/index.css";
const props = defineProps<{
  items: Object;
}>();
</script>

<template>
  <JsonViewer :value="props.items" copyable boxed sort theme="light"  />
</template>

<style scoped></style>
