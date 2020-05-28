<template>
  <div class="app-container">
    <!-- <Button>你好</Button> -->
    <el-table :data="tableData3" style="width: 100%">
      <el-table-column width="120" prop="date" label="nihao"></el-table-column>
      <el-table-column prop="name" label="姓名" width="120"></el-table-column>
      <el-table-column label="地址">
        <el-table-column prop="province" label="省份" width="120"></el-table-column>
        <el-table-column prop="city" label="市区" width="120"></el-table-column>
        <el-table-column prop="address" label="地址" width="300"></el-table-column>
        <el-table-column prop="zip" label="邮编" width="120"></el-table-column>
      </el-table-column>
    </el-table>
  </div>
</template>
<script>
export default {
  filters: {},
  data () {
    return {
      tableData3: [
        {
          date: '2016-05-03',
          name: '王小虎',
          province: '上海',
          city: '普陀区',
          address: '上海市普陀区金沙江路 1518 弄',
          zip: 200333,
        }
      ]
    }
  },
  created () {},
  methods: {}
}
</script>
<style>
.app-container{
  padding-left: 20px;
}
.el-table thead.is-group th {
  background: #fff;
}

.el-table thead.is-group tr:first-of-type th:first-of-type:before {
  content: "日期";
  text-align: center;
  position: absolute;
  width: 152px;
  height: 1px;
  bottom: 30px;
  right: 22px;
}
.el-table thead.is-group tr:first-of-type th:first-of-type:after {
  content: "配送新增";
  text-align: center;
  position: absolute;
  width: 152px;
  top: 9px;
  left: 0;
} 
.el-table thead.is-group tr:first-of-type th:first-of-type .cell {
  position: absolute;
  top: 0;
  left: 0;
  width: 152px;
  height: 30px;
  /* background-color: #ebeef5; */
  /* border-right-width: 1px;
  border-left-width: 1px;
  border-left-color: black;
  border-right-color: black; */
  border:1px solid #ebeef5;
  display: block;
  text-align: center;
  transform: rotate(35deg);
  transform-origin: top left;
  -ms-transform: rotate(35deg);
  -ms-transform-origin: top left;
  -webkit-transform: rotate(35deg);
  -webkit-transform-origin: top left;
}

/* .el-table thead.is-group tr:first-of-type th:first-of-type .cell2 {
  position: absolute;
  top: 10;
  left: 10;
  width: 152px;
  height: 1px;
  background-color: red;
  display: block;
  text-align: center;
  transform: rotate(30deg);
  transform-origin: top left;
  -ms-transform: rotate(30deg);
  -ms-transform-origin: top left;
  -webkit-transform: rotate(30deg);
  -webkit-transform-origin: top left;
} */
/* .el-table thead.is-group tr:first-of-type th:first-of-type:before {
  content: "日期";
  text-align: center;
  position: absolute;
  width: 152px;
  height: 1px;
  bottom: 30px;
  right: 22px;
}
.el-table thead.is-group tr:first-of-type th:first-of-type:after {
  content: "配送新增";
  text-align: center;
  position: absolute;
  width: 152px;
  top: 20px;
  left: 0;
}
.el-table thead.is-group tr:first-of-type th:first-of-type .sadasda {
  position: absolute;
  top: 30px;
  left: 30px;
  width: 300px;
  height: 7px;
  background-color: red;
  display: block;
} */

</style>
