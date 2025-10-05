<script setup lang="ts">
import MatrixSlot from "./MatrixSlot.vue";
import AboutDropContent from "./AboutDropContent.vue";
import AboutDropHeader from "./AboutDropHeader.vue";
import PromotionBlock from "./PromotionBlock.vue";
</script>

<template>
  <div class="matrix-about">
    <h2 class="matrix-about__title">1. Общая информация</h2>
    <div class="matrix-about__drop">
      <AboutDropHeader />
      <AboutDropContent />
    </div>
    <MatrixSlot />
    <PromotionBlock />
  </div>
</template>

<style lang="less" scoped>
.matrix-about {
  display: flex;
  flex-direction: column;
  max-width: 932px;
  @media (max-width: @mobile) {
    max-width: 100%;
  }
  &__title {
    font-size: 2rem;

    font-weight: 900;
    line-height: 40px;
    @media (max-width: @mobile) {
      font-size: 1.75rem;
      line-height: 32px;
    }
    margin-bottom: 32px;
  }
  &__drop {
    border-radius: 44px;
    border: 1px solid rgba(236, 236, 236, 1);
    display: flex;
    flex-direction: column;
    gap: 16px;
  }
}
</style>
