<template>
  <d2-container :filename="filename">
    <template slot="header">流体高度</template>
    <d2-crud
      :columns="columns"
      :data="data"
      :options="options"
      :rowHandle="rowHandle"/>
    <el-card shadow="never" class="d2-mb">
      <d2-markdown :source="doc"/>
    </el-card>
    <el-card shadow="never" class="d2-mb">
      <d2-highlight :code="code"/>
    </el-card>
    <template slot="footer">
      <d2-link-btn title="文档" link="https://doc.d2admin.fairyever.com/zh/ecosystem-d2-crud/"/>
    </template>
  </d2-container>
</template>

<script>
import doc from './doc.md'
import code from './code.js'

export default {
  data () {
    return {
      filename: __filename,
      doc,
      code,
      columns: [
        {
          title: '日期',
          key: 'date'
        },
        {
          title: '姓名',
          key: 'name'
        },
        {
          title: '省份',
          key: 'province'
        },
        {
          title: '市区',
          key: 'city'
        },
        {
          title: '地址',
          key: 'address',
          width: '300'
        },
        {
          title: '邮编',
          key: 'zip'
        }
      ],
      data: [
        {
          date: '2016-05-03',
          name: '王小虎',
          province: '上海',
          city: '普陀区',
          address: '上海市普陀区金沙江路 1518 弄',
          zip: 200333
        },
        {
          date: '2016-05-02',
          name: '王小虎',
          province: '上海',
          city: '普陀区',
          address: '上海市普陀区金沙江路 1518 弄',
          zip: 200333
        },
        {
          date: '2016-05-04',
          name: '王小虎',
          province: '上海',
          city: '普陀区',
          address: '上海市普陀区金沙江路 1518 弄',
          zip: 200333
        },
        {
          date: '2016-05-01',
          name: '王小虎',
          province: '上海',
          city: '普陀区',
          address: '上海市普陀区金沙江路 1518 弄',
          zip: 200333
        },
        {
          date: '2016-05-08',
          name: '王小虎',
          province: '上海',
          city: '普陀区',
          address: '上海市普陀区金沙江路 1518 弄',
          zip: 200333
        },
        {
          date: '2016-05-06',
          name: '王小虎',
          province: '上海',
          city: '普陀区',
          address: '上海市普陀区金沙江路 1518 弄',
          zip: 200333
        },
        {
          date: '2016-05-07',
          name: '王小虎',
          province: '上海',
          city: '普陀区',
          address: '上海市普陀区金沙江路 1518 弄',
          zip: 200333
        }
      ],
      options: {
        maxHeight: '250'
      },
      rowHandle: {
        remove: {
          size: 'mini',
          confirm: false
        }
      }
    }
  }
}
</script>
