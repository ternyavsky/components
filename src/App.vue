<script setup lang="ts">
import Matrix from "./components/Matrix.vue";
</script>

<template>
  <div class="layout">
    <Matrix />
  </div>
</template>

<style lang="less" scoped>
@import "./styles/variables.less";
.layout {
  background-color: var(--color-default-bg);
  padding: 47px 48px;
  border-radius: 40px;
  min-height: 100vh;

  @media (max-width: @tablet) {
    padding: 24px 16px;
    border-radius: 20px;
  }

  @media (max-width: @mobile) {
    border-radius: 0;
    padding: 0px;
  }

  @media (min-width: @large-desktop) {
    padding: 60px 60px;
    max-width: 1920px;
    margin: 0 auto;
  }
}
</style>
