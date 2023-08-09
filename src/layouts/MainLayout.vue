<template>
  <div>
    <n-space size="large" justify="space-between">
      <span>btn to main</span><span>btn to menu</span>
    </n-space>
  </div>
  <n-layout has-sider embedded class="sidebar-layout">
    <n-space vertical size="large">
      <n-layout-header class="header-sidebar-layout"> </n-layout-header>
      <n-layout-sider
        class="sidebar-container"
        bordered
        collapse-mode="width"
        :show-collapsed-content="false"
        show-trigger="arrow-circle"
      >
        <div v-for="row in ['row1', 'row2', 'row3']" :key="row">
          {{ row }}
        </div>
      </n-layout-sider>
    </n-space>
    <n-layout-content>
      <div>some content</div>
    </n-layout-content>
  </n-layout>
</template>

<script setup lang="ts">
import { NSpace, NLayout, NLayoutSider, NLayoutContent } from "naive-ui";
</script>
