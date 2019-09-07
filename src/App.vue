<template>
  <div id="app">


    <div class="container">
      <hot-table 
        :data="data" 
        :colHeaders="colHeaders" 
        :rowHeaders="rowHeaders" 
        :stretchH='stretchH'
        ></hot-table>
    </div>


  </div>
</template>

<script>
import { HotTable } from "@handsontable/vue";

export default {
  name: "app",
  data() {
    return {
      data: [
        ["", "Tesla", "Mercedes", "Toyota", "Volvo"],
        ["2019", 10, 11, 12, 13],
        ["2020", 20, 11, 14, 13],
        ["2021", 30, 15, 12, 13]
      ],
      colHeaders: ['A', 'B', 'asd'],
      rowHeaders:['asd','dsf','dgdg','asd'],
      stretchH:'all'
    };
  },
  components: {
    HotTable
  },
  mounted() {
    // console.log(this.$refs.HOTTABLE);
  }
};
</script>

<style src="../node_modules/handsontable/dist/handsontable.full.css">
</style>

<style lang='less'>
#app {
  border: 2px solid pink;

  .container {
    border: 1px solid cyan;
    width: 500px;
    height: 500px;
    overflow: hidden;
  }
}
</style>