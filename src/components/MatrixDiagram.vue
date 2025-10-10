<template>
  <div class="matrix-diagram">
    <div class="matrix-diagram__text">
      <h2 class="matrix-diagram__title">Круговая диаграмма</h2>
      <p class="matrix-diagram__description">
        Круговая диаграмма - это графическое отображение вашей Матрицы судьбы.
        Она удобно представляет результаты всех расчётов и служит основой для
        дальнейшей расшифровки.
      </p>
    </div>
    <img
      class="matrix-diagram__img"
      src="/src/assets/diagram.svg"
      alt="Диаграмма"
    />
  </div>
</template>

<style lang="less" scoped>
@import "../styles/variables.less";
.matrix-diagram {
  background-color: @color-default-grey;
  border-radius: 32px;
  padding: 0px 32px;
  align-items: center;
  display: flex;
  gap: 24px;
  max-width: 932px;

  @media (max-width: @laptop) {
    padding: 0px 24px;
    gap: 20px;
    max-width: 100%;
  }

  @media (max-width: @tablet) {
    flex-direction: column;
    gap: 18px;
    padding: 24px 16px;
    max-width: 100%;
    border-radius: 24px;
  }

  @media (max-width: @mobile) {
    flex-direction: column;
    gap: 16px;
    padding: 32px 16px;
    max-width: 100%;
    margin: 0px 16px;
  }
  &__text {
    display: flex;
    flex-direction: column;
    gap: 16px;

    @media (max-width: @tablet) {
      gap: 12px;
    }
  }

  &__title {
    font-size: 1.5rem;
    line-height: 32px;
    font-weight: 900;

    @media (max-width: @laptop) {
      font-size: 1.375rem;
      line-height: 30px;
    }

    @media (max-width: @tablet) {
      font-size: 1.25rem;
      line-height: 28px;
      text-align: center;
    }

    @media (max-width: @mobile) {
      font-size: 1.125rem;
      line-height: 26px;
    }
  }

  &__description {
    font-size: 1.0625rem;
    line-height: 28px;
    font-weight: 700;
    color: @color-black-main;

    @media (max-width: @laptop) {
      font-size: 1rem;
      line-height: 26px;
    }

    @media (max-width: @tablet) {
      font-size: 0.9rem;
      line-height: 24px;
      text-align: center;
    }

    @media (max-width: @mobile) {
      font-size: 0.875rem;
      line-height: 22px;
      font-weight: 600;
    }
  }

  &__img {
    padding: 32px 0px 32px 32px;
    width: 100%;
    height: 100%;
    object-fit: contain;

    @media (max-width: @laptop) {
      padding: 24px 0px 24px 24px;
    }

    @media (max-width: @tablet) {
      padding: 16px 0px;
      max-width: 300px;
      margin: 0 auto;
    }

    @media (max-width: @mobile) {
      padding: 0px;
      margin: 0 auto;
      max-width: 250px;
    }
  }
}
</style>
