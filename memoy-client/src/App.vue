<template>
  <div id="app">
    <div>
      <el-row>

        <el-col :span="4">&nbsp;</el-col>

        <el-col :span="16">
          <!-- 导航栏 -->
          <el-menu
            class="el-menu"
            active-text-color="orange"
            :default-active="activeIndex"
            mode="horizontal"
            @select="handleSelect">
            <el-menu-item><span style="color: orange;font-size:25px;font-family: 黑体">记账猫🐱</span></el-menu-item>
            <el-menu-item style="float: right;">
              <el-avatar shape="square" :size="mini"
                         src="https://timgsa.baidu.com/timg?image&quality=80&size=b9999_10000&sec=1561652718625&di=563350d3010ccb6c2911f71098322633&imgtype=0&src=http%3A%2F%2Fcdn.lizhi.fm%2Fradio_cover%2F2014%2F08%2F06%2F13521050432793220.jpg"></el-avatar>
            </el-menu-item>
            <el-menu-item index="2" style="float:right;">报表</el-menu-item>
            <el-menu-item index="1" style="float:right;"><i class="el-icon-plus"></i></el-menu-item>
          </el-menu>
        </el-col>

        <el-col :span="4">&nbsp;</el-col>

      </el-row>

    </div>

    <!-- iframe路由页面显示区域-->
    <div style="margin-top:20px;">
      <el-row>

        <el-col :span="4">&nbsp;</el-col>

        <el-col :span="16">
          <router-view/>
        </el-col>

        <el-col :span="4">&nbsp;</el-col>
      </el-row>
    </div>

  </div>
</template>

<script>
  export default {
    name: 'App',
    data() {
      return {
        activeIndex: '1',
        templates: '{{productDate}}'
      };
    },
    methods: {
      handleSelect(key, keyPath) {

        console.log(key, keyPath);
        let Mytemplates = this.templates.replace(/\{{productDate}}/g, '2015-2-2');
        console.log(Mytemplates);
      }
    }
  }
</script>

<style>

</style>
