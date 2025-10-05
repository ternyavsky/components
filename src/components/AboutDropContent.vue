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

  &__title {
    font-size: 1.5rem;
    font-weight: 900;
    line-height: 32px;
  }
  &__description {
    font-size: 1.0625rem;
    font-weight: 700;
    line-height: 28px;
    color: @color-black-main;
  }

  &__state-block {
    display: flex;
    flex-direction: column;
    gap: 28px;
    margin-top: 26px;
    @media (max-width: @mobile) {
      margin-top: 16px;
      gap: 16px;
    }
  }
}
</style>
