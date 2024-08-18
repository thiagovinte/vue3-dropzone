<template>
  <div
    class="app"
    style="width: 478px; height: 200px"
  >
    <Vue3Dropzone
      v-model="files"
      @error="showError"
    />
  </div>
</template>

<script setup>
import Vue3Dropzone from "./components/Vue3Dropzone.vue";
import { ref, watch } from "vue";

const files = ref([]);
const showError = (data) => {
  console.log("error", data);
};
</script>

<style lang="scss" scoped></style>
