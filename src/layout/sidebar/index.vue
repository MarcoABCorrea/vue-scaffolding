<template>
  <div id="sidebar">
    <logo />
    <el-scrollbar id="sidebar-scroll">
      <sidebar-menu />
    </el-scrollbar>
  </div>
</template>

<script lang="ts">
  import SidebarMenu from '@/layout/sidebar/sidebarMenu/index.vue'
  import Logo from './sidebarMenu/logo.vue'
  import { Component, Prop, Vue } from 'vue-property-decorator'

  @Component({
    components: { SidebarMenu, Logo }
  })
  export default class Sidebar extends Vue {}
</script>

<style lang="scss" scoped>
  #sidebar {
    flex-shrink: 0;
    display: flex;
    flex-direction: column;
    transition: width 0.3s;
    background-color: #393942;
    width: 65px;
    height: 100vh;
    position: fixed;
    z-index: 800;
    overflow-x: hidden;

    #sidebar-scroll {
      flex: 1;
    }

    .el-scrollbar__bar.is-horizontal {
      display: none;
    }

    enu-icon {
      margin-right: 25px;
    }

    &:hover:not(.nest-menu-item) {
      border-left: #ff5533;
      border-width: 0 0 0 2px;
      border-style: solid;
    }

    #sidebar-menu:not(.el-menu--collapse) {
      .el-submenu__title {
        span {
          &::after {
            content: '+';
            float: right;
          }
        }
      }
    }

    .nest-menu-item {
      .el-submenu__title {
        span {
          &::after {
            content: '+' !important;
            float: right !important;
          }
        }
      }

      .el-submenu__title,
      .el-menu-item {
        background-color: #2a2a32 !important;

        &:hover {
          background-color: #22222a !important;
        }
      }
    }
  }
</style>
