<template>
  <div id="sidebar-logo">
    <img src="@/assets/logo.svg" alt="" />
  </div>
</template>

<script lang="ts">
  import { Vue } from 'vue-property-decorator'

  export default class Logo extends Vue {}
</script>

<style lang="scss" scoped>
  #sidebar-logo {
    min-height: 50px;
    display: flex;
    align-items: center;
    justify-content: center;
    overflow: hidden;

    img {
      width: 32px;
      height: 32px;
    }
  }
</style>
