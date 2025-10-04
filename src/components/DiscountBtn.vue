<script setup lang="ts"></script>
<template>
  <div class="discount-btn">
    <p class="discount-btn__text">Открыть всю матрицу судьбы</p>
    <div class="discount-btn__price">
      <p class="discount-btn__price__old">477 ₽</p>
      <p class="discount-btn__price__new">
        <span class="discount-btn__price__new__desktop">за </span>37₽
      </p>
    </div>
  </div>
</template>
<style lang="less" scoped>
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
  @media (max-width: @mobile) {
    padding: 8px 8px 8px 20px;
  }
  &__text {
    font-size: 20px;
    font-weight: 800;
    line-height: 20px;
    color: var(--color-default-bg);
    @media (max-width: @mobile) {
      font-size: 16px;
      line-height: 18px;
    }
  }
  &__price {
    padding: 8px 8px 8px 10px;
    background: var(--color-default-bg);
    border-radius: 12px;
    display: flex;
    flex-direction: row;
    align-items: center;
    justify-content: center;
    gap: 12px;
    @media (max-width: @mobile) {
      padding: 8px 8px 8px 10px;
    }
    &__old {
      font-weight: 700;
      font-size: 14px;
      line-height: 16px;
      color: #000;
      position: relative;
      padding-top: 4px;

      &::after {
        content: "";
        position: absolute;
        top: 50%;
        left: 0;
        right: 0;
        height: 1px;
        background-color: var(--color-purple-main);
        transform: rotate(11deg);
        transform-origin: center;
      }
    }
    &__new {
      font-weight: 900;
      font-size: 20px;
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
    }

    &__new__desktop {
      @media (max-width: @mobile) {
        display: none;
      }
    }
  }
}
</style>
