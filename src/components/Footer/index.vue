<template>
  <div class="footer">
    <div class="footer-content">
      <el-row :gutter="20">
        <el-col :span="6"
          ><div />
          地址：下沙一坊95号102室</el-col
        >
        <el-col :span="6"
          ><div />
          联系电话：17688827766</el-col
        >
        <el-col :span="6"
          ><div />
          工作时间:上午9点~下午6点</el-col
        >
        <el-col :span="6"
          ><div />
          邮箱：xu_dreamer@sina.com</el-col
        >
      </el-row>
      <el-divider class="divider" />
      <p>
        Copyright © 2023,深圳联威发科技有限公司 版权所有
        备案号：粤ICP备2021037301号 未经同意不得转载
      </p>
    </div>
  </div>
</template>

<script setup></script>

<style scoped>
.footer {
  /* position: absolute; */
  bottom: 0;
  width: 100%;
  background-color: #1b252e;
  color: #8b939d;
  text-align: center;
  display: flex;
  justify-content: center;
  padding: 100px 0;
}

.footer-content {
  width: 60%;
}
</style>
