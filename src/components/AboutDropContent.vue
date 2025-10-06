<script setup lang="ts">
import AddBlock from "./AddBlock.vue";
import DiscountBtn from "./DiscountBtn.vue";
import StateBlock from "./StateBlock.vue";
</script>

<template>
  <div class="about-drop-content">
    <h2 class="about-drop-content__title">
      Визитная карточка: характер человека в плюсе и минусе
    </h2>
    <p class="about-drop-content__description">
      Это своего рода, «визитная карточка»: характер и личные качества, которые
      человек получает в момент рождения. Как и всё другое в Матрице судьбы,
      этот аспект имеет как положительный, так и отрицательный вариант развития.
      Хотя на практике плюсы и минусы находятся в некой неравной пропорции.
      Соответственно, положительные моменты нужно развивать, а отрицательные
      прорабатывать или, как минимум знать о них, и стараться нивелировать.
    </p>
    <AddBlock />
    <DiscountBtn />

    <div class="about-drop-content__state-block">
      <StateBlock />
    </div>
  </div>
</template>

<style lang="less" scoped>
@import "../styles/variables.less";
.about-drop-content {
  display: flex;
  flex-direction: column;
  padding: 24px 32px 32px 32px;
  gap: 16px;

  @media (max-width: @laptop) {
    padding: 20px 24px 28px 24px;
    gap: 14px;
  }

  @media (max-width: @tablet) {
    padding: 18px 20px 24px 20px;
    gap: 12px;
  }

  @media (max-width: @mobile) {
    padding: 16px 16px 20px 16px;
    gap: 10px;
  }

  &__title {
    font-size: 1.5rem;
    font-weight: 900;
    line-height: 32px;

    @media (max-width: @laptop) {
      font-size: 1.375rem;
      line-height: 30px;
    }

    @media (max-width: @tablet) {
      font-size: 1.25rem;
      line-height: 28px;
    }

    @media (max-width: @mobile) {
      font-size: 1.125rem;
      line-height: 26px;
    }
  }

  &__description {
    font-size: 1.0625rem;
    font-weight: 700;
    line-height: 28px;
    color: @color-black-main;

    @media (max-width: @laptop) {
      font-size: 1rem;
      line-height: 26px;
    }

    @media (max-width: @tablet) {
      font-size: 0.9rem;
      line-height: 24px;
    }

    @media (max-width: @mobile) {
      font-size: 0.875rem;
      line-height: 22px;
    }
  }

  &__state-block {
    display: flex;
    flex-direction: column;
    gap: 28px;
    margin-top: 26px;

    @media (max-width: @laptop) {
      gap: 24px;
      margin-top: 22px;
    }

    @media (max-width: @tablet) {
      gap: 20px;
      margin-top: 18px;
    }

    @media (max-width: @mobile) {
      margin-top: 16px;
      gap: 16px;
    }
  }
}
</style>
