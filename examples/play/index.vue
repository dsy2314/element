<template>
  <div style="margin: 20px;">
    <el-table
      :data="tableData"
      size=""
      width=""
      height="300"
      max-height="300"
      :fit="true"
      :stripe="false"
      :border="true"
      row-key="id"
      context=""
      :show-header="true"
      :show-summary="false"
      sum-text=""
      :summary-method="() => {}"
      row-class-name=""
      :row-style="() => ''"
      cell-class-name=""
      :cell-style="() => ''"
      :header-row-class-name="headerRowClassName"
      :header-row-style="headerRowStyle"
      header-cell-class-name=""
      :header-cell-style="() => ''"
      :highlight-current-row="false"
      current-row-key=""
      empty-text=""
      :expand-row-keys="[]"
      :default-expand-all="false"
      :default-sort="{}"
      tooltip-effect=""
      :span-method="() => {}"
      :select-on-indeterminate="true"
      :indent="16"
      :tree-props="{ hasChildren: 'hasChildren', children: 'children'}"
      :lazy="false"
      :load="() => {}"
      style="width: 100%">
      <el-table-column
        type="default"
        label="日期"
        class-name=""
        label-class-name=""
        prop="date"
        width="180"
        min-width="180"
        :sortable="false"
        :sort-method="() => {}"
        sort-by=""
        :resizable="true"
        column-key=""
        align=""
        header-align=""
        :show-tooltip-when-overflow="true"
        :show-overflow-tooltip="true"
        :fixed="false"
        :formatter="(row, column, cellValue) => cellValue"
        :selectable="() => {}"
        :reserve-selection="false"
        :filter-method="() => {}"
        :filtered-value="[]"
        :filters="[]"
        filter-placement=""
        :filter-multiple="true"
        :index="() => {}"
        :sort-orders="['ascending', 'descending', null]"
      >
      </el-table-column>
      <el-table-column
        prop="name"
        label="姓名"
        width="180">
      </el-table-column>
      <el-table-column
        prop="address"
        label="地址">
      </el-table-column>
      <el-table-column label="哈哈">
        <template slot-scope="scope">
          <span>{{getValue(scope)}}</span>
        </template>
      </el-table-column>
    </el-table>
  </div>
</template>

<script>
  export default {
    data() {
      return {
        tableData: [{
          id: 1,
          date: '2016-05-02',
          name: '王小虎',
          address: '上海市普陀区金沙江路 1518 弄'
        }, {
          id: 2,
          date: '2016-05-04',
          name: '王小虎',
          address: '上海市普陀区金沙江路 1517 弄'
        }, {
          id: 3,
          date: '2016-05-01',
          name: '王小虎',
          address: '上海市普陀区金沙江路 1519 弄'
        }, {
          id: 4,
          date: '2016-05-03',
          name: '王小虎',
          address: '上海市普陀区金沙江路 1516 弄'
        }]
      };
    },
    methods: {
      getValue(data) {
        // console.log(data);
        return "hello"
      },

      headerRowStyle({rowIndex}) {
        console.log({rowIndex});
        return "haha";
      },

      headerRowClassName({rowIndex}){
        console.log({rowIndex});
        return "emm";
      }
    }
  };
</script>
