<script setup lang="ts"></script>
<template>
  <div class="promotion-block">
    <div class="promotion-block__main-text">
      <h2 class="promotion-block__title">Открыть всю матрицу судьбы</h2>
      <p class="promotion-block__price">37 ₽</p>
    </div>
    <p class="promotion-block__subtitle">До конца скидки:</p>
    <div class="promotion-block__timer">
      <p class="promotion-block__timer-time">
        29<span class="promotion-block__timer-unit"> м</span>:59<span
          class="promotion-block__timer-unit"
        >
          с</span
        >
      </p>
      <div class="promotion-block__old-price">
        <p class="promotion-block__old-price-title">Старая цена:</p>
        <p class="promotion-block__old-price-value">547 ₽</p>
      </div>
    </div>
    <div class="promotion-block__btn">
      <p>Открыть матрицу</p>
    </div>
  </div>
</template>
<style lang="less" scoped>
@import "../styles/variables.less";
.promotion-block {
  background-image: url("/src/assets/promotion.svg");
  display: flex;
  flex-direction: column;
  width: 468px;
  padding: 16px;
  height: object-fit;
  object-fit: contain;
  border-radius: 28px;
  &__main-text {
    display: flex;
    justify-content: space-between;
    align-items: center;
  }
  &__title {
    color: @color-default-bg;
    max-width: 220px;
    font-size: 1.5rem;
    font-weight: 900;
    line-height: 28px;
  }
  &__price {
    font-size: 4.875rem;
    font-weight: 900;
    line-height: 78px;
    letter-spacing: -4%;
    color: @color-yellow-main;
  }
  &__subtitle {
    font-size: 0.75rem;
    font-weight: 700;
    line-height: 24px;
    color: @color-default-bg;
  }
  &__timer {
    display: flex;
    flex-direction: row;
    align-items: center;
    justify-content: space-between;
  }
  &__timer-time {
    font-weight: 800;
    line-height: 28px;
    font-size: 1.75rem;
    color: @color-yellow-main;
    letter-spacing: 1px;
  }
  &__timer-unit {
    font-size: 0.75rem;
    font-weight: 700;
    line-height: 20px;
    display: inline-block;
    margin-top: 4px;
  }
  &__old-price {
    display: flex;
    flex-direction: column;
    align-items: flex-end;
    color: @color-default-bg;
  }
  &__old-price-title {
    font-size: 0.75rem;
    font-weight: 700;
    line-height: 16px;
  }
  &__old-price-value {
    font-size: 1.5rem;
    font-weight: 900;
    line-height: 28px;
    text-decoration: line-through;
  }
  &__btn {
    margin-top: 16px;
    border-radius: 12px;
    text-align: center;
    background-color: @color-default-bg;
    padding: 12px 16px;
    width: 100%;
    font-size: 1.25rem;
    font-weight: 800;
    line-height: 24px;
    &:hover {
      animation: ease-out 0.3s;
      cursor: pointer;
      transform: scale(1.05);
    }
  }
}
</style>
