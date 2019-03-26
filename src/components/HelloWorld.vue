<template>
  <el-tabs v-model="activeName" @tab-click="handleClick">
    <el-tab-pane label="数据图" name="first"></el-tab-pane>
    <el-tab-pane label="统计表" name="second"></el-tab-pane>
  </el-tabs>
</template>
<script>

  export default {
    data() {
      return {
        activeName: 'first'
      };
    },
    watch : {
    'activeName':function(val) { //监听切换状态-表格
          let urlStr = '.\Table.vue';
          this.$router.push(urlStr);
          // 注释，根据val的不同，跳转到不同
      },
    },
    methods: {
      handleClick(tab, event) {
        console.log(tab, event);
      }
    }
  };
</script>
