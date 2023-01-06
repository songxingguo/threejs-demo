<script setup>
import { RouterLink, RouterView } from "vue-router";
</script>

<template>
  <el-container>
    <el-aside width="200px">
      <el-menu>
        <el-sub-menu index="1">
          <template #title>
            <el-icon>
              <message />
            </el-icon>导航
          </template>
          <el-menu-item-group>
            <el-menu-item index="1-1">
              <router-link to="/">基本操作</router-link>
            </el-menu-item>
            <el-menu-item index="1-2">
              <router-link to="/about">立方体</router-link>
            </el-menu-item>
          </el-menu-item-group>
        </el-sub-menu>
      </el-menu>
    </el-aside>
    <el-container>
      <el-main>
        <router-view></router-view>
      </el-main>
    </el-container>
  </el-container>
</template>

<style scoped>
</style>
