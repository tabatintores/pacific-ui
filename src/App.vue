<template>
  <PacificGeoLayout>
    <template #header>
      <el-page-header content="Pacific UI Test Header" />
    </template>

    <template #left>
      <el-menu>
        <el-menu-item index="1">Menu Item 1</el-menu-item>
        <el-menu-item index="2">Menu Item 2</el-menu-item>
        <el-menu-item index="3">Menu Item 3</el-menu-item>
      </el-menu>
    </template>

    <template>
      <el-card>
        <h2>Main Content</h2>
        <p>This is the main content area.</p>
      </el-card>
    </template>

    <template #right>
      <el-card>
        <h2>Right Sidebar</h2>
        <p>Additional info or actions.</p>
      </el-card>
    </template>

    <template #footer>
      <el-footer>Test Footer © 2024</el-footer>
    </template>
  </PacificGeoLayout>
</template>

<script setup>
import PacificGeoLayout from './lib-components/layouts/PacificGeoLayout.vue';
</script>
