
<script lang="ts">
import NavBox from './NavBox.vue';
import Navbar from './Navbar.vue';
import QuillEditor from './QuillEditor.vue'
import InputForm from './InputForm.vue'
import InputDatepicker from './InputDatepicker.vue'
import InputFile from './InputFile.vue';    

export default {
name: "Layout",
components: {
    Navbar,
    QuillEditor,
    InputForm,
    InputDatepicker,
    InputFile,
    NavBox
}, 
data() {
    return {
      navBoxes: [
        {
          caption: 'Admin',
          items: [
            { text: 'Adminstuff1', link: '#' },
            { text: 'Adminstuff2', link: '#' },
          ],
        },
        {
          caption: 'Navigation',
          items: [
            { text: 'Nav 1', link: '#' },
            { text: 'Nav 2', link: '#' },
          ],
        },
      ],
    };
  },
};

</script>

<template>
    <Navbar/>

    <div class="container-fluid mt-5">
    <div class="row mt-5">
      <!-- Left Side (Stackable Divs) -->
      <div class="col-md-3">
        <NavBox
          v-for="(item, index) in navBoxes"
          :key="index"
          :caption="item.caption"
          :items="item.items"
        />
      </div>
      <div class="col-md-9">
        
        <InputDatepicker label="Berichte von" inputId="ReportDate"/>
        <InputForm
      label="Bericht über"
      inputId="ReportSubject"
      inputPlaceholder="Bericht über"
    />
      <!-- Main Component (Text Editor) -->
      <QuillEditor/>
      
      <InputFile/>
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