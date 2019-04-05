<template>
  <div class="grid-container">
    <div class="grid-header">
      <div v-for="(header, idx) in gridSchema" :key="idx">
        {{header.field}}
      </div>
    </div>
    <div class="grid-body">
      <div v-for="(data, idx) in gridData" class="grid-row" :key="idx">
         {{data.column1}}
         {{data.column2}}
         {{data.column3}}
         {{data.column4}}
         {{data.column5}}
         {{data.column6}}
         {{data.column7}}
         {{data.column8}}
      </div>
    </div>
  </div>
</template>

<script>

export default {
  name: 'grid',
  props: {
    gridSchema: { type: Array, required: true}, 
    gridData: { type: Array, required: true}
  } 
}

</script>

<style>
</style>