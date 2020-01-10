<template>
  <div id="sidebar-activator">
    <i class="el-icon-s-unfold"></i>
  </div>
</template>

<script lang="ts">
  import { Vue } from 'vue-property-decorator'

  export default class SidebarActivator extends Vue {}
</script>

<style lang="scss" scoped>
  #sidebar-activator {
    width: 50px;
    text-align: center;
    line-height: 50px;
    padding-left: 10px;
    transition: padding-left 0.3s;

    #activator-icon {
      transition: transform 0.3s;

      &.activator-turn {
        transform: rotate(-180deg);
      }
    }
  }
</style>
