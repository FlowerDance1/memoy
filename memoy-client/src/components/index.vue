<template>
  <div>
    <el-row>
      <!--<el-col>
        <el-image
          style="width: 100px;height: 100px;"
          src="https://timgsa.baidu.com/timg?image&quality=80&size=b9999_10000&sec=1561652718625&di=563350d3010ccb6c2911f71098322633&imgtype=0&src=http%3A%2F%2Fcdn.lizhi.fm%2Fradio_cover%2F2014%2F08%2F06%2F13521050432793220.jpg"
          :fit="fit"
        ></el-image>
      </el-col>-->

      <!--      <el-col :span="3"><span>&nbsp;</span></el-col>-->
      <el-col>
        <el-menu
          class="el-menu"

          active-text-color="orange"
          :default-active="activeIndex"
          mode="horizontal"
          @select="handleSelect">

          <el-menu-item>
            <el-image
              style="width: 50px;height: 50px;"
              src="https://timgsa.baidu.com/timg?image&quality=80&size=b9999_10000&sec=1561652718625&di=563350d3010ccb6c2911f71098322633&imgtype=0&src=http%3A%2F%2Fcdn.lizhi.fm%2Fradio_cover%2F2014%2F08%2F06%2F13521050432793220.jpg"
              :fit="fit"
            ></el-image>
          </el-menu-item>

          <el-menu-item index="1">
            <i class="el-icon-plus"></i>
          </el-menu-item>
          <el-menu-item index="2">报表分析</el-menu-item>
          <el-menu-item index="3">流水账</el-menu-item>
          <el-menu-item index="4">我的</el-menu-item>
        </el-menu>
      </el-col>

    </el-row>


  </div>

</template>

<script>
  export default {
    name: 'index',
    data() {
      return {
        activeIndex: '1',
        templates:'{{productDate}}'
      };
    },
    methods: {
      handleSelect(key, keyPath) {

       // console.log(key, keyPath);
        let Mytemplates = this.templates.replace(/\{{productDate}}/g, '2015-2-2');
        console.log(Mytemplates);
      }
    }
  }
</script>

<style scoped>

</style>
