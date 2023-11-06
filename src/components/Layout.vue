
<script lang="ts">
import Navbar from './Navbar.vue';
import QuillEditor from './QuillEditor.vue'
import InputForm from './InputForm.vue'
export default {
name: "Layout",
components: {
    Navbar,
    QuillEditor,
    InputForm,
}, 
    data() {
    return {
      stackableItems: ['Admin', 'x', 'x'], // Replace with your actual data
    };
},
};

</script>

<template>
    <Navbar/>

    <div class="container-fluid mt-5">
    <div class="row">
      <!-- Left Side (Stackable Divs) -->
      <div class="col-md-3">
        <div class="stackable-div" v-for="(item, index) in stackableItems" :key="index">
          {{ item }}
        </div>
      </div>
      <div class="col-md-9">
        <InputForm
      label="Bericht über"
      inputId="customInputId"
      inputPlaceholder="Bericht über"
    />
      <!-- Main Component (Text Editor) -->
      <QuillEditor/>
      </div>
    </div>
  </div>
</template>

<style scoped>
.stackable-div {
  border: 1px solid #ccc;
  padding: 10px;
  margin: 5px 0;
}
</style>