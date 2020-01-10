<template>
  <div id="toolbar">
    <sidebar-activator />
    <div class="spacer"></div>
  </div>
</template>

<script lang="ts">
  import { Vue, Component } from 'vue-property-decorator'
  import SidebarActivator from '@/layout/outside/toolbar/sidebarActivator.vue'

  @Component({
    components: { SidebarActivator }
  })
  export default class Toolbar extends Vue {}
</script>

<style lang="scss" scoped>
  #toolbar {
    background: lightblue;
    height: 50px;
    display: inline-flex;
    flex-wrap: nowrap;
  }

  .spacer {
    flex: 1;
  }
</style>
