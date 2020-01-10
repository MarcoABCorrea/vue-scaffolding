<template>
  <el-menu
    id="sidebar-menu"
    :background-color="'#393942'"
    text-color="grey"
    :collapse="!sidebarOpen"
    active-text-color="#ffb286"
    :collapse-transition="false"
  >
    <sidebar-menu-item
      v-for="route in routes"
      :key="route.fullPath"
      :route="route"
    />
  </el-menu>
</template>

<script lang="ts">
  import SidebarMenuItem from '@/layout/sidebar/sidebarMenu/sidebarMenuItem.vue'
  import { Component, Prop, Vue } from 'vue-property-decorator'

  @Component({ components: { SidebarMenuItem } })
  export default class SidebarMenu extends Vue {
    sidebarOpen = false
    routes = [
      {
        fullPath: '/',
        name: 'Home'
      }
    ]
  }
</script>

<style lang="scss" scoped>
  #sidebar-menu {
    width: 100%;
  }
</style>
