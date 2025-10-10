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

  @media (max-width: @laptop) {
    width: 400px;
    border-radius: 24px;
    padding: 14px;
  }

  @media (max-width: @tablet) {
    width: 100%;
    max-width: 350px;
    border-radius: 20px;
    padding: 12px;
  }

  @media (max-width: @mobile) {
    width: 100%;
    border-radius: 16px;
    padding: 10px;
  }
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

    @media (max-width: @laptop) {
      font-size: 1.25rem;
      line-height: 24px;
      max-width: 180px;
    }

    @media (max-width: @tablet) {
      font-size: 1.125rem;
      line-height: 22px;
      max-width: 160px;
    }

    @media (max-width: @mobile) {
      font-size: 1rem;
      line-height: 20px;
      max-width: 140px;
    }
  }

  &__price {
    font-size: 4.875rem;
    font-weight: 900;
    line-height: 78px;
    letter-spacing: -4%;
    color: @color-yellow-main;

    @media (max-width: @laptop) {
      font-size: 4rem;
      line-height: 64px;
    }

    @media (max-width: @tablet) {
      font-size: 3.5rem;
      line-height: 56px;
    }

    @media (max-width: @mobile) {
      font-size: 3rem;
      line-height: 48px;
    }
  }
  &__subtitle {
    font-size: 0.75rem;
    font-weight: 700;
    line-height: 24px;
    color: @color-default-bg;

    @media (max-width: @tablet) {
      font-size: 0.7rem;
      line-height: 20px;
    }
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

    @media (max-width: @laptop) {
      font-size: 1.5rem;
      line-height: 24px;
    }

    @media (max-width: @tablet) {
      font-size: 1.25rem;
      line-height: 22px;
    }

    @media (max-width: @mobile) {
      font-size: 1.125rem;
      line-height: 20px;
    }
  }

  &__timer-unit {
    font-size: 0.75rem;
    font-weight: 700;
    line-height: 20px;
    display: inline-block;
    margin-top: 4px;

    @media (max-width: @tablet) {
      font-size: 0.7rem;
      line-height: 18px;
    }
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

    @media (max-width: @tablet) {
      font-size: 0.7rem;
      line-height: 14px;
    }
  }

  &__old-price-value {
    font-size: 1.5rem;
    font-weight: 900;
    line-height: 28px;
    text-decoration: line-through;

    @media (max-width: @laptop) {
      font-size: 1.25rem;
      line-height: 24px;
    }

    @media (max-width: @tablet) {
      font-size: 1.125rem;
      line-height: 22px;
    }

    @media (max-width: @mobile) {
      font-size: 1rem;
      line-height: 20px;
    }
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

    @media (max-width: @laptop) {
      font-size: 1.125rem;
      line-height: 22px;
      padding: 10px 14px;
    }

    @media (max-width: @tablet) {
      font-size: 1rem;
      line-height: 20px;
      padding: 8px 12px;
      border-radius: 10px;
    }

    @media (max-width: @mobile) {
      font-size: 0.9rem;
      line-height: 18px;
      padding: 8px 10px;
      border-radius: 8px;
    }

    &:hover {
      cursor: pointer;
    }
  }
}
</style>
