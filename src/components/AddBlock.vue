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

      <AddBlockCard :is-lock="false" />
      <AddBlockCard :is-lock="true" />
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

  @media (max-width: @laptop) {
    gap: 14px;
    margin-top: 30px;
  }

  @media (max-width: @tablet) {
    gap: 12px;
    margin-top: 26px;
    flex-direction: column;
  }

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

    @media (max-width: @laptop) {
      max-width: 250px;
      max-height: 250px;
      border-radius: 28px;
    }

    @media (max-width: @tablet) {
      max-width: 200px;
      max-height: 200px;
      border-radius: 24px;
    }

    @media (max-width: @mobile) {
      max-width: 150px;
      max-height: 150px;
      border-radius: 20px;
    }
  }

  &__subtitle {
    display: flex;
    flex-direction: column;
  }

  &__subtitle__title {
    font-size: 1.5rem;
    font-weight: 700;
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

  &__subtitle__subtitle {
    font-size: 1.75rem;
    font-weight: 800;
    line-height: 32px;

    @media (max-width: @laptop) {
      font-size: 1.5rem;
      line-height: 30px;
    }

    @media (max-width: @tablet) {
      font-size: 1.375rem;
      line-height: 28px;
    }

    @media (max-width: @mobile) {
      font-size: 1.25rem;
      line-height: 26px;
    }
  }

  &__subtitle__description {
    margin-top: 16px;
    font-size: 1.0625rem;
    font-weight: 700;
    line-height: 28px;
    color: @color-black-main;

    @media (max-width: @laptop) {
      font-size: 1rem;
      line-height: 26px;
      margin-top: 14px;
    }

    @media (max-width: @tablet) {
      font-size: 0.9rem;
      line-height: 24px;
      margin-top: 12px;
    }

    @media (max-width: @mobile) {
      font-size: 0.875rem;
      line-height: 22px;
      font-weight: 600;
      margin-top: 10px;
    }
  }
}
</style>
