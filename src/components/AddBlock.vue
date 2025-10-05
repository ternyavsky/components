<script setup lang="ts">
import AddBlockCard from "./AddBlockCard.vue";
</script>

<template>
  <div class="about-drop-content__add-block">
    <div class="about-drop-content__add-block__subtitle">
      <h3 class="about-drop-content__add-block__subtitle__title">8 аркан</h3>
      <h2 class="about-drop-content__add-block__subtitle__subtitle">
        Справедливость
      </h2>
      <p class="about-drop-content__add-block__subtitle__description">
        Такой человек не подвержен эмоциям, умеет усмирять свои чувства и
        спокойно подходить к решению любых проблем. При принятии решений
        руководствуется логикой и фактами, старается быть максимально справедлив
        и честен, как с самим собой, так и с окружающими. Всегда соблюдает
        закон, не любит что-то нарушать.
      </p>

      <AddBlockCard />
    </div>
    <img
      src="/src/assets/drop-content-girl.svg"
      alt="drop-content-girl"
      class="about-drop-content__add-block__img"
    />
  </div>
</template>
<style lang="less" scoped>
@import "../styles/variables.less";
.about-drop-content__add-block {
  display: flex;
  flex-direction: row;
  gap: 16px;
  margin-top: 34px;
  @media (max-width: @mobile) {
    flex-direction: column;
    margin-top: 24px;
  }
  &__img {
    max-width: 308px;
    max-height: 308px;
    border-radius: 32px;
    width: 100%;
    height: 100%;
    object-fit: contain;
    margin: 0 auto;
  }
  &__subtitle {
    display: flex;
    flex-direction: column;
  }
  &__subtitle__title {
    font-size: 1.5rem;
    font-weight: 700;
    line-height: 32px;
  }
  &__subtitle__subtitle {
    font-size: 1.75rem;
    font-weight: 800;
    line-height: 32px;
  }
  &__subtitle__description {
    margin-top: 16px;
    font-size: 1.0625rem;
    font-weight: 700;
    line-height: 28px;
    color: @color-black-main;
    @media (max-width: @mobile) {
      font-size: 0.875rem;
      line-height: 22px;
      font-weight: 600;
    }
  }
}
</style>
