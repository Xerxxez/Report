<script lang="ts">
import { RouterLink, RouterView } from 'vue-router'
import Layout from './components/Layout.vue';

export default {
  name: 'App',
  components: {
    Layout,
  },
};

</script>

<template>
   <div id="app">
    <Layout/>
   </div>
</template>

<style scoped>
.div{
background-color: blanchedalmond;
}

</style>
