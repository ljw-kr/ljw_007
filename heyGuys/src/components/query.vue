<template>
<div>
    <div class="top">
    <el-input v-model="input" placeholder="   请输入查询内容" style="width:160px"></el-input>
    <i class="el-icon-search top-icon"></i>
    </div>
     <el-table
    :data="tableData"
    style="width: 100%"
    :default-sort = "{prop: 'date', order: 'descending'}"
    >
    <el-table-column
      prop="date"
      label="日期"
      sortable
      width="180">
    </el-table-column>
    <el-table-column
      prop="name"
      label="姓名"
      sortable
      width="180">
    </el-table-column>
    <el-table-column
      prop="address"
      label="地址"
      :formatter="formatter">
    </el-table-column>
  </el-table>
</div>

</template>
<script>
/* eslint-disable */
export default {
     data () {
      return {
          input:'',
        tableData: [{
          date: '2016-05-02',
          name: '王小虎',
          address: '上海市普陀区金沙江路 1518 弄'
        }, {
          date: '2016-05-04',
          name: '黄大星',
          address: '上海市普陀区金沙江路 1517 弄'
        }, {
          date: '2016-05-01',
          name: '张大师',
          address: '上海市普陀区金沙江路 1519 弄'
        }, {
          date: '2016-05-03',
          name: '葛二蛋',
          address: '上海市普陀区金沙江路 1516 弄'
        }]
      }
    },
    methods: {
      formatter(row, column) {
        return row.address;
      }
    }
}
</script>
<style scoped>
  .top{
      float: left;
      position: relative;
  }
  .top .top-icon{
      position: absolute;
      left: 10px;
      top: 12px;
      z-index: 2;
  }
</style>
