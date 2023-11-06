<template>
  <QuillEditor toolbar="#my-toolbar">
    <template #toolbar>
      <div id="my-toolbar">
        <!-- Add buttons as you would before -->
        <button class="ql-bold"></button>
        <button class="ql-italic"></button>
        <!-- But you can also add your own -->
        <button id="custom-button"></button>
      </div>
    </template>
  </QuillEditor>
  </template>
  <script lang="ts">
import '@vueup/vue-quill/dist/vue-quill.snow.css';
import { QuillEditor } from '@vueup/vue-quill';
export default {
   components:{ 
    QuillEditor
},
};
</script>