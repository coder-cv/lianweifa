<template>
  <div class="header">
    <div class="header-left" @click="logoClick">
      <img class="company-logo" src="../../assets/img/company_logo.jpg" />
      <div class="company-info">
        <div class="company-name">深圳市联威发科技有限公司</div>
        <div class="header-title">lianweifa.com</div>
      </div>
    </div>
    <el-menu
      :default-active="activeIndex"
      menu-trigger="click"
      text-color="#333"
      style="height: 65px; border: 0"
      mode="horizontal"
      @select="handleSelect"
      :ellipsis="false"
      class="nav-bar"
    >
      <el-menu-item index="1" class="header-title">首页</el-menu-item>
      <el-sub-menu index="2">
        <template #title>产品中心</template>
        <el-menu-item index="2-1">风扇</el-menu-item>
        <el-menu-item index="2-2">空心杯电机</el-menu-item>
        <el-menu-item index="2-3">轮毂电机</el-menu-item>
        <el-menu-item index="2-4">激光雷达</el-menu-item>
      </el-sub-menu>
      <el-menu-item index="4" class="header-title">合作伙伴</el-menu-item>
      <el-menu-item index="5" class="header-title">关于我们</el-menu-item>
    </el-menu>
    <div class="header-right">咨询服务电话:18682474935(微信同号)</div>
  </div>
  <div class="container" style="clear: both">
    <router-view></router-view>
  </div>

  <el-backtop :right="100" :bottom="100" />
</template>

<script setup>
import { ref } from "vue";
const activeIndex = ref("1");

const handleSelect = (index) => {
  activeIndex.value = index;
};
</script>

<style l scoped>
.header {
  height: 65px;
  display: flex;
}

.header-left {
  width: 300px;
  display: flex;
  align-items: center;
  justify-content: center;
  margin-left: 40px;
}

.header-left .company-logo {
  width: 50px;
  height: 50px;
}

.nav-bar {
  flex: 1;
  justify-content: center;
}

.header-right {
  width: 300px;
  display: flex;
  align-items: center;
  justify-content: center;
  margin-right: 40px;
}

.back-to-top {
  position: fixed;
  bottom: 50px;
  right: 30px;
  cursor: pointer;
}

a {
  text-decoration: none;
}
a:visited {
  text-decoration: none;
}
a:hover {
  text-decoration: none;
}
a:active {
  text-decoration: none;
}
</style>
