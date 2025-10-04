<script setup lang="ts"></script>
<template>
  <div class="promotion-block">
    <div class="promotion-block__main-text">
      <h2 class="promotion-block__main-text__title">
        Открыть всю матрицу судьбы
      </h2>
      <p class="promotion-block__main-text__price">37 ₽</p>
    </div>
    <p class="promotion-block__discount-subtitle">До конца скидки:</p>
    <div class="promotion-block__discount-timer">
      <p class="promotion-block__discount-timer__time">
        29<span class="promotion-block__discount-timer__time__unit"> м</span
        >:59<span class="promotion-block__discount-timer__time__unit"> с</span>
      </p>
      <div class="promotion-block__discount-timer__old-price">
        <p class="promotion-block__discount-timer__old-price__title">
          Старая цена:
        </p>
        <p class="promotion-block__discount-timer__old-price__price">547 ₽</p>
      </div>
    </div>
    <div class="promotion-block__btn">
      <p>Открыть матрицу</p>
    </div>
  </div>
</template>
<style lang="less" scoped>
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
    &__title {
      color: var(--color-default-bg);
      max-width: 220px;
      font-size: 24px;
      font-weight: 900;
      line-height: 28px;
    }
    &__price {
      font-size: 78px;
      font-weight: 900;
      line-height: 78px;
      letter-spacing: -4%;
      color: var(--color-yellow-main);
    }
  }
  &__discount-subtitle {
    font-size: 12px;
    font-weight: 700;
    line-height: 24px;
    color: var(--color-default-bg);
  }
  &__discount-timer {
    display: flex;
    flex-direction: row;
    align-items: center;
    justify-content: space-between;
    &__time {
      font-weight: 800;
      line-height: 28px;
      font-size: 28px;
      color: var(--color-yellow-main);
      letter-spacing: 1px;

      &__unit {
        font-size: 12px;
        font-weight: 700;
        line-height: 20px;
        display: inline-block;
        margin-top: 4px;
      }
    }
    &__old-price {
      display: flex;
      flex-direction: column;
      align-items: flex-end;
      color: var(--color-default-bg);
      &__title {
        font-size: 12px;
        font-weight: 700;
        line-height: 16px;
      }
      &__price {
        font-size: 24px;
        font-weight: 900;
        line-height: 28px;
        text-decoration: line-through;
      }
    }
  }
  &__btn {
    margin-top: 16px;
    border-radius: 12px;
    text-align: center;
    background-color: var(--color-default-bg);
    padding: 12px 16px;
    width: 100%;
    font-size: 20px;
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
