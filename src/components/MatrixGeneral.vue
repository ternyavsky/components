<template>
  <div class="matrix-general">
    <div class="matrix-general__container">
      <h2 class="matrix-general__title">Общая матрица</h2>
      <div class="matrix-general__description">
        <p>
          Метод расчёта Матрицы Судьбы объединяет многовековые знания
          классической астрологии, нумерологические законы и мудрость Старших
          Арканов Таро. Это уникальный инструмент для погружения в тайны вашей
          личности, который через дату рождения раскрывает неочевидные грани
          характера, скрытые таланты и ключевые жизненные уроки. Как натальная
          карта или квадрат Пифагора, матрица помогает системно взглянуть на
          вашу судьбу, но делает это через призму символов, чисел и архетипов,
          создавая многомерную картину вашего пути.
        </p>
        <p>
          Глубина анализа поражает: вы увидите не только базовые тенденции, но и
          энергетические паттерны, которые влияют на отношения, карьеру, финансы
          и духовный рост. В отличие от поверхностных гороскопов, здесь акцент
          делается на комплексном подходе — каждая деталь взаимосвязана, как
          шестерёнки часового механизма.
        </p>
      </div>
    </div>
    <div class="matrix-general__bg"></div>
  </div>
</template>

<style lang="less" scoped>
@import "../styles/variables.less";
.matrix-general {
  &__bg {
    position: absolute;
    top: 150px;
    left: 98px;
    width: 932px;
    height: 621px;
    background-image: linear-gradient(
        to bottom,
        rgba(255, 255, 255, 0.79),
        rgba(255, 255, 255, 1)
      ),
      url("/src/assets/matrix-numbers.jpg");
    background-size: 100% 100%, cover;
    background-position: center, center;
    background-repeat: no-repeat;
    z-index: 1;

    @media (max-width: @laptop) {
      width: 60%;
      height: 400px;
      left: 20%;
      top: 120px;
      max-width: 500px;
      display: none;
    }

    @media (max-width: @tablet) {
      width: 50%;
      height: 300px;
      left: 25%;
      top: 100px;
      max-width: 350px;
      display: none;
    }

    @media (max-width: 600px) {
      display: none;
    }

    @media (max-width: @mobile) {
      display: none;
    }
  }
}
.matrix-general__container {
  position: relative;
  margin-top: 36px;
  display: flex;
  background-color: @color-default-bg;
  border: 1px solid rgba(236, 236, 236, 1);
  flex-direction: column;
  padding: 32px;
  border-radius: 16px;
  gap: 16px;
  z-index: 2;
  max-height: fit-content;
  overflow: hidden;

  @media (max-width: @laptop) {
    padding: 28px;
    margin-top: 32px;
  }

  @media (max-width: @tablet) {
    padding: 20px;
    margin-top: 24px;
    border-radius: 12px;
  }

  @media (max-width: @mobile) {
    padding: 16px;
    margin-top: 20px;
  }
  &__title {
    font-size: 2rem;
    font-weight: 800;
    line-height: 36px;
    position: relative;

    &::after {
      content: " судьбы";
    }

    @media (max-width: @laptop) {
      font-size: 1.75rem;
      line-height: 32px;
    }

    @media (max-width: @tablet) {
      font-size: 1.5rem;
      line-height: 28px;
    }

    @media (max-width: @mobile) {
      font-size: 1.25rem;
      line-height: 24px;
      &::after {
        display: none;
      }
    }
  }

  &__description {
    display: flex;
    flex-direction: column;
    font-size: 1.0625rem;
    gap: 28px;

    @media (max-width: @laptop) {
      font-size: 1rem;
      gap: 24px;
    }

    @media (max-width: @tablet) {
      font-size: 0.9rem;
      gap: 20px;
    }

    @media (max-width: @mobile) {
      font-size: 0.875rem;
      gap: 16px;
    }
  }
}
</style>
