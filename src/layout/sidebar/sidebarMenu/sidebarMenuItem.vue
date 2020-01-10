<template>
  <div class="sidebar-menu-item">
    <template>
      <router-link :to="'home'">
        <el-menu-item>
          <i class="el-icon-s-home"></i>
        </el-menu-item>
      </router-link>
    </template>
  </div>
</template>

<script lang="ts">
  import { Component, Prop, Vue } from 'vue-property-decorator'

  @Component
  export default class SidebarMenuItem extends Vue {
    @Prop() private route!: any
    sidebarOpen = false
  }
</script>

<style scoped lang="scss"></style>
