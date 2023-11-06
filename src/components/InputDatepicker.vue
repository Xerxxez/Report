<template>
<label :for="inputId" class="form-label">{{ label }}</label>
    <VueDatePicker v-model="date"></VueDatePicker>
  </template>
  
  <script lang="ts">
  import VueDatePicker from '@vuepic/vue-datepicker';
  import '@vuepic/vue-datepicker/dist/main.css'
  
  export default {
    components: { VueDatePicker },
    props: {
        label: String,             
        inputId: String,           
    },
    data() {
      return {
        date: null,
      };
    }
  }
  </script>