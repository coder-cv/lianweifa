<template>
  <el-carousel height="550px">
    <el-carousel-item v-for="(item, index) in banner" :key="index">
      <img :src="getAssetUrl(item.img)" class="banner-img" />
    </el-carousel-item>
  </el-carousel>

  <div class="product">
    <div class="product-title">产品中心</div>
    <el-menu
      :default-active="activeIndex"
      background-color="#545c64"
      class="el-menu-vertical-demo"
      text-color="#fff"
      menu-trigger="click"
      @select="handleSelect"
      :ellipsis="false"
    >
      <el-menu-item index="1" class="header-title">风扇</el-menu-item>
      <el-menu-item index="2" class="header-title">空心杯电机</el-menu-item>
      <el-menu-item index="3" class="header-title">轮毂电机</el-menu-item>
      <el-menu-item index="4" class="header-title">激光雷达</el-menu-item>
    </el-menu>
  </div>
  <div class="partner">
    <div class="partner-title">合作伙伴</div>
    <div class="partner-parent">
      <div class="partner-item" v-for="item in partner" :key="item.id">
        <img :src="getAssetUrl(item.img)" />
      </div>
    </div>
  </div>

  <div class="about">
    <div class="about-title">关于我们</div>
    <div class="about-content">
      <p class="about-me-p">
        公司业务：散热风扇、空心杯电机、轮毂电机、激光雷达等产品。
      </p>
      <p class="about-me-p">公司宗旨：为客户提供最高品质的产品与服务。</p>
    </div>
  </div>
</template>

<script setup>
import banner from "@/assets/data/banner.js";
import partner from "@/assets/data/partner.js";
import { getAssetUrl } from "@/utils/load_assets.js";
</script>

<style>
.banner-img {
  height: 550px;
  width: 100%;
}

.partner {
  margin-top: 30px;
  width: 100%;
}

.partner-parent {
  display: flex;
  justify-content: center;
  width: 90%;
  margin: 20px auto;
  align-items: center;
  height: auto;
}
.partner-item {
  margin: 0 20px;
  text-align: center;
}

.product-title,
.partner-title,
.about-title {
  display: flex;
  margin-top: 30px;
  width: 100%;
  justify-content: center;
  font-size: 24px;
}

.about-content {
  background-color: #f2f6fc;
  margin: 30px auto;
  width: 90%;
  padding: 20px;
}

.about-me-p {
  font-size: 24px;
  font-weight: normal;
  padding: 10px;
}
</style>
