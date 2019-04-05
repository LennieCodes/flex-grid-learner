<template>
  <div id="app">
    <Grid :grid-data="gridData" :grid-schema="gridSchema" /> 
  </div>
</template>

<script>
import Grid from '@/components/Grid';
import gridData from '@/json/gridData.json';
import gridSchema from '@/json/gridSchema.json';

export default {
  name: 'app',
  components: {
    Grid,
  },
  data() {
    return {
      gridData,
      gridSchema,
    }
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
