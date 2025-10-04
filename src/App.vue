<script setup lang="ts">
import Matrix from "./components/Matrix.vue";
</script>

<template>
  <div class="layout">
    <Matrix />
  </div>
</template>

<style lang="less" scoped>
.layout {
  background-color: var(--color-default-bg);
  padding: 47px 48px;
  border-radius: 40px;
  @media (max-width: @mobile) {
    border-radius: 0;
    padding: 0px;
  }
}
</style>
