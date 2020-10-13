<template>
  <div id="app">
    <el-table :data="tableData" style="width: 100%">
      <el-table-column label="日期" width="180">
        <editable-cell slot-scope="{ row }" :can-edit="true" v-model="row.date">
          <span slot="content">{{ row.date }}</span>
        </editable-cell>
      </el-table-column>
      <el-table-column label="姓名" width="180">
        <editable-cell slot-scope="{ row }" :can-edit="true" v-model="row.name">
          <span slot="content">{{ row.name }}</span>
        </editable-cell>
      </el-table-column>
      <el-table-column label="地址">
        <editable-cell
          slot-scope="{ row }"
          :can-edit="true"
          v-model="row.address"
        >
          <span slot="content">{{ row.address }}</span>
        </editable-cell>
      </el-table-column>
    </el-table>
  </div>
</template>
<script>
import editableCell from "./components/editableCell.vue";
export default {
  components: {
    editableCell
  },
  data() {
    return {
      tableData: [
        {
          date: "2016-05-02",
          name: "王小虎",
          address: "上海市普陀区金沙江路 1518 弄"
        },
        {
          date: "2016-05-04",
          name: "王小虎",
          address: "上海市普陀区金沙江路 1517 弄"
        },
        {
          date: "2016-05-01",
          name: "王小虎",
          address: "上海市普陀区金沙江路 1519 弄"
        },
        {
          date: "2016-05-03",
          name: "王小虎",
          address: "上海市普陀区金沙江路 1516 弄"
        }
      ]
    };
  }
};
</script>

<style lang="less">
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
</style>
