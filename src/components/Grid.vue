<template>
  <div class="grid-container">
    <div class="grid-header">
      <div v-for="(header, idx) in gridSchema" :key="idx"
        :style="{'width': `${header.width}%`}">
        {{header.field}}
      </div>
    </div>
    <div class="grid-body">
      <div v-for="(data, idx) in gridData" 
        class="grid-row" 
        :key="idx">
         <span :style="{'width': getDataFieldWidth(0)}">{{data.column1}}</span>
         <span :style="{'width': getDataFieldWidth(1)}">{{data.column2}}</span>
         <span :style="{'width': getDataFieldWidth(2)}">{{data.column3}}</span>
         <span :style="{'width': getDataFieldWidth(3)}">{{data.column4}}</span>
         <span :style="{'width': getDataFieldWidth(4)}">{{data.column5}}</span>
         <span :style="{'width': getDataFieldWidth(5)}">{{data.column6}}</span>
         <span :style="{'width': getDataFieldWidth(6)}">{{data.column7}}</span>
         <span :style="{'width': getDataFieldWidth(7)}">{{data.column8}}</span>
         <span :style="{'width': getDataFieldWidth(8)}">{{data.column9}}</span>
         <span :style="{'width': getDataFieldWidth(9)}">{{data.column10}}</span>
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
  },
  methods: {
    getDataFieldWidth(idx) {
      return `${this.gridSchema[idx].width}%`;
    }
  } 
}

</script>

<style lang="scss">

.grid-container {
  .grid-row, .grid-header {
    display: flex;
  }
}
</style>