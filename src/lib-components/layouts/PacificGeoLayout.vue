<template>
  <el-container class="geo-layout">
    <el-header v-if="$slots.header" height="60px" class="geo-layout__header">
      <slot name="header" />
    </el-header>

    <el-container>
      <el-aside v-if="isLeftVisible" width="200px" class="geo-layout__left">
        <slot name="left" />
      </el-aside>

      <el-main class="geo-layout__center">
        <slot />
      </el-main>

      <el-aside v-if="isRightVisible" width="200px" class="geo-layout__right">
        <slot name="right" />
      </el-aside>
    </el-container>

    <el-footer v-if="$slots.footer" height="60px" class="geo-layout__footer">
      <slot name="footer" />
    </el-footer>
  </el-container>
</template>

<script setup>
defineProps({
  isLeftVisible: { type: Boolean, default: true },
  isRightVisible: { type: Boolean, default: true }
});
</script>

<style scoped>
.geo-layout {
  height: 100vh;
}

.geo-layout__header, .geo-layout__footer {
  background-color: #f5f5f5;
}

.geo-layout__left, .geo-layout__right {
  background-color: #e0e0e0;
  padding: 16px;
}

.geo-layout__center {
  padding: 16px;
}
</style>
