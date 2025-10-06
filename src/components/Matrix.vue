<script setup lang="ts">
import MatrixContents from "./MatrixContents.vue";
import MatrixGeneral from "./MatrixGeneral.vue";
import MatrixDiagram from "./MatrixDiagram.vue";
import MatrixAbout from "./MatrixAbout.vue";
import MatrixMaintenance from "./MatrixMaintenance.vue";
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
      <MatrixMaintenance />
  </div>
</template>

<style lang="less" scoped>
@import "../styles/variables.less";
.matrix-text {
  display: flex;
  flex-direction: column;
  gap: 8px;

  @media (max-width: @tablet) {
    padding: 40px 0px;
  }

  @media (max-width: @mobile) {
    padding: 72px 16px;
  }

  &__title {
    font-size: 3rem;
    font-weight: 800;
    line-height: 60px;

    @media (max-width: @laptop) {
      font-size: 2.5rem;
      line-height: 50px;
    }

    @media (max-width: @tablet) {
      font-size: 2rem;
      line-height: 40px;
    }

    @media (max-width: @mobile) {
      font-size: 1.5rem;
      line-height: 28px;
    }
  }

  &__description {
    font-size: 1rem;
    font-weight: 700;
    color: @color-subtitle;

    @media (max-width: @tablet) {
      font-size: 0.9rem;
    }
  }
}
.matrix-info {
  display: flex;
  flex-direction: row;
  gap: 48px;

  @media (max-width: @laptop) {
    gap: 32px;
  }

  @media (max-width: @tablet) {
    flex-direction: column;
    gap: 24px;
  }

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

  @media (max-width: @laptop) {
    gap: 32px;
    margin-top: 40px;
  }

  @media (max-width: @tablet) {
    flex-direction: column;
    gap: 24px;
    margin-top: 32px;
  }

  &__about {
    display: flex;
    flex-direction: column;
    gap: 48px;

    @media (max-width: @laptop) {
      gap: 32px;
    }

    @media (max-width: @tablet) {
      gap: 24px;
    }

    @media (max-width: @mobile) {
      gap: 24px;
    }
  }
}
</style>
