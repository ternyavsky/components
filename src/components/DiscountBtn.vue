<script setup lang="ts"></script>
<template>
  <div class="discount-btn">
    <p class="discount-btn__text">Открыть всю матрицу судьбы</p>
    <div class="discount-btn__price">
      <p class="discount-btn__old-price">477 ₽</p>
      <p class="discount-btn__new-price">
        <span class="discount-btn__new-price-desktop">за </span>37₽
      </p>
    </div>
  </div>
</template>
<style lang="less" scoped>
@import "../styles/variables.less";
.discount-btn {
  background: linear-gradient(
    90deg,
    rgba(255, 104, 217, 1) 0%,
    rgba(176, 112, 255, 1) 100%
  );
  border-radius: 20px;
  width: 100%;
  padding: 8px 0px;
  gap: 13px;
  display: flex;
  flex-direction: row;
  align-items: center;
  justify-content: center;
  cursor: pointer;

  @media (max-width: @laptop) {
    border-radius: 18px;
    gap: 12px;
    padding: 6px 6px;
  }

  @media (max-width: @tablet) {
    border-radius: 16px;
    gap: 10px;
    padding: 8px 12px 8px 20px;
  }

  @media (max-width: @mobile) {
    padding: 8px 12px 8px 20px;
    border-radius: 14px;
  }

  &__text {
    font-size: 1.25rem;
    font-weight: 800;
    line-height: 20px;
    color: @color-default-bg;

    @media (max-width: @laptop) {
      font-size: 1.125rem;
      line-height: 19px;
    }

    @media (max-width: @tablet) {
      font-size: 1rem;
      line-height: 18px;
    }

    @media (max-width: @mobile) {
      font-size: 1rem;
      line-height: 18px;
    }
  }
  &__price {
    padding: 8px 12px 8px 10px;
    background: @color-default-bg;
    border-radius: 12px;
    display: flex;
    flex-direction: row;
    align-items: center;
    justify-content: center;
    gap: 12px;
    min-width: 80px;

    @media (max-width: @laptop) {
      border-radius: 10px;
      gap: 10px;
      padding: 6px 10px 6px 8px;
      min-width: 70px;
    }

    @media (max-width: @tablet) {
      border-radius: 8px;
      gap: 8px;
      padding: 6px 8px 6px 8px;
      min-width: fit-content;
    }

    @media (max-width: @mobile) {
      padding: 6px 8px 6px 8px;
      border-radius: 8px;
      min-width: fit-content;
      gap: 6px;
    }
  }
  &__old-price {
    font-weight: 700;
    font-size: 0.875rem;
    line-height: 16px;
    color: #000;
    position: relative;
    padding-top: 4px;

    @media (max-width: @laptop) {
      font-size: 0.8rem;
      line-height: 15px;
    }

    @media (max-width: @tablet) {
      font-size: 0.65rem;
      line-height: 14px;
      padding-top: 3px;
      min-width: fit-content;
    }

    @media (max-width: @mobile) {
      font-size: 0.7rem;
      line-height: 12px;
    }

    &::after {
      content: "";
      position: absolute;
      top: 50%;
      left: 0;
      right: 0;
      height: 1px;
      background-color: @color-purple-main;
      transform: rotate(11deg);
      transform-origin: center;
    }
  }
  &__new-price {
    font-weight: 900;
    font-size: 1.25rem;
    line-height: 28px;
    background: linear-gradient(
      90deg,
      rgba(255, 104, 217, 1) 0%,
      rgba(176, 112, 255, 1) 100%
    );
    -webkit-background-clip: text;
    background-clip: text;
    -webkit-text-fill-color: transparent;
    color: transparent;

    @media (max-width: @laptop) {
      font-size: 1.125rem;
      line-height: 26px;
    }

    @media (max-width: @tablet) {
      font-size: 1rem;
      line-height: 24px;
    }

    @media (max-width: @mobile) {
      font-size: 0.9rem;
      line-height: 20px;
    }
  }

  &__new-price-desktop {
    @media (max-width: @tablet) {
      display: none;
    }

    @media (max-width: @mobile) {
      display: none;
    }
  }
}
</style>
