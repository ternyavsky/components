<script setup lang="ts">
import MatrixContents from "./MatrixContents.vue";
import MatrixGeneral from "./MatrixGeneral.vue";
import MatrixDiagram from "./MatrixDiagram.vue";
import MatrixAbout from "./MatrixAbout.vue";
</script>

<template>
  <div class="matrix">
    <div class="matrix-text">
      <h2 class="matrix-text__title">Матрица судьбы</h2>
      <p class="matrix-text__description">
        Матрица судьбы онлайн: расчёт с полной расшифровкой
      </p>
    </div>
    <div class="matrix-info">
      <MatrixGeneral />
      <MatrixContents />
    </div>

    <div class="matrix-main">
      <div class="matrix-main__about">
        <MatrixDiagram />
        <MatrixAbout />
      </div>
    </div>
  </div>
</template>

<style lang="less" scoped>
.matrix-text {
  display: flex;
  flex-direction: column;
  gap: 8px;
  @media (max-width: @mobile) {
    padding: 72px 16px;
  }
  &__title {
    font-size: 48px;
    font-weight: 800;
    line-height: 60px;
    @media (max-width: @mobile) {
      font-size: 24px;
      line-height: 28px;
    }
  }
  &__description {
    font-size: 16px;
    font-weight: 700;
    color: var(--color-subtitle);
  }
}
.matrix-info {
  display: flex;
  flex-direction: row;
  gap: 48px;
  @media (max-width: @mobile) {
    flex-direction: column;
    gap: 683px;
  }
}
.matrix-main {
  display: flex;
  flex-direction: row;
  gap: 48px;
  margin-top: 50px;
  &__about {
    display: flex;
    flex-direction: column;
    gap: 48px;
    @media (max-width: @mobile) {
      gap: 24px;
    }
  }
}
</style>
