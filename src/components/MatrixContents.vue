<script setup lang="ts">
import matrixImg from "/src/assets/matrix-contents-girl.svg";
import lockIcon from "/src/assets/lock.svg";
</script>

<template>
  <div class="matrix-contents-container">
    <div class="matrix-contents">
      <div class="matrix-contents__title">Оглавление</div>
      <div class="matrix-contents__list">
        <div class="matrix-contents__section">
          <div class="matrix-contents__section-title">1. Общая информация</div>
          <div class="matrix-contents__items">
            <div class="matrix-contents__item">
              1.1 Характер человека в плюсе и минусе
            </div>
            <div class="matrix-contents__item">
              1.2 Кармический хвост и задачи прошлой жизни
            </div>
            <div class="matrix-contents__item">
              1.3 Проработка души в нынешнем воплощении
            </div>
            <div class="matrix-contents__item">
              1.4 Главные задачи души до 40 лет
            </div>
            <div class="matrix-contents__item">
              1.5 Точка гармонии и душевного комфорта
            </div>
            <div class="matrix-contents__item">
              1.6 Родовые программы по линиям отца и матери
            </div>
            <div class="matrix-contents__item">
              1.7 Врождённые таланты человека
            </div>
            <div class="matrix-contents__item">
              1.8 Детско-родительская карма
            </div>
          </div>
        </div>

        <div class="matrix-contents__section">
          <div class="matrix-contents__section-title">2. Предназначение</div>
          <div class="matrix-contents__items">
            <div class="matrix-contents__item">
              2.1 Личное предназначение человека
            </div>
            <div class="matrix-contents__item">
              2.2 Социальное предназначение человека
            </div>
            <div class="matrix-contents__item">
              2.3 Духовное предназначение человека
            </div>
          </div>
        </div>

        <div class="matrix-contents__section">
          <div class="matrix-contents__section-title">3. Отношения</div>
          <div class="matrix-contents__items">
            <div class="matrix-contents__item">
              3.1 Встреча и готовность к отношениям
            </div>
            <div class="matrix-contents__item">
              3.2 Общий характер отношений с партнёром
            </div>
            <div class="matrix-contents__item">
              3.3 Проблемы и способы их решения
            </div>
          </div>
        </div>

        <div class="matrix-contents__section">
          <div class="matrix-contents__section-title">4. Деньги и карьера</div>
          <div class="matrix-contents__items">
            <div class="matrix-contents__item">
              4.1 Общее состояние и кармические задачи
            </div>
            <div class="matrix-contents__item">
              4.2 Финансовый потенциал и профессии
            </div>
            <div class="matrix-contents__item">
              4.3 Денежный поток: блокировка и развитие
            </div>
          </div>
        </div>
        <div class="matrix-contents__items">
          <div class="matrix-contents__item">5 Чакровая карта здоровья</div>
          <div class="matrix-contents__item">6 Прогноз по годам жизни</div>
        </div>
      </div>

      <div class="matrix-contents__disclaimer">
        Нажимая на кнопку, вы соглашаетесь с нашими
        <a href="#" class="matrix-contents__link">правилами </a>
        <a href="#" class="matrix-contents__link"
          >обработки персональных данных</a
        >.
      </div>
    </div>
    <div class="matrix-transcription">
      <img
        :src="matrixImg"
        alt="matrix-transcription"
        class="matrix-transcription__img"
      />
      <h2 class="matrix-transcription__title">
        Ждет ли вас успех в 2025 году?
      </h2>
      <p class="matrix-transcription__description">
        Ответ уже записан в вашей натальной карте, зарегистрируйтесь, чтобы
        узнать
      </p>
      <div class="matrix-transcription__button">
        <img
          :src="lockIcon"
          alt="lock"
          class="matrix-transcription__button-icon"
        />
        <p class="matrix-transcription__button-text">Расшифровать</p>
      </div>
    </div>
  </div>
</template>

<style lang="less" scoped>
@import "../styles/variables.less";
.matrix-contents-container {
  display: flex;
  flex-direction: column;
  min-width: 500px;
  gap: 28px;

  @media (max-width: @laptop) {
    min-width: 400px;
    gap: 24px;
  }

  @media (max-width: @tablet) {
    min-width: 100%;
    gap: 20px;
  }

  @media (max-width: @mobile) {
    min-width: 100%;
    gap: 16px;
  }
  .matrix-contents {
    background-color: @color-default-grey;
    padding: 16px;
    border-radius: 28px;
    display: flex;
    flex-direction: column;
    gap: 16px;
    &__title {
      background-color: rgba(255, 255, 255, 1);
      border-radius: 16px;
      padding: 12px 0px 8px 16px;
      font-size: 1.75rem;
      font-weight: 900;
      line-height: 36px;

      @media (max-width: @laptop) {
        font-size: 1.5rem;
        line-height: 32px;
      }

      @media (max-width: @tablet) {
        font-size: 1.25rem;
        line-height: 28px;
        text-align: center;
      }

      @media (max-width: @mobile) {
        text-align: center;
      }
    }

    &__list {
      display: flex;
      flex-direction: column;
      gap: 16px;
      @media (min-width: @desktop) {
        padding: 0px 16px;
      }
    }

    &__section {
      display: flex;
      flex-direction: column;
      gap: 8px;
    }

    &__section-title {
      font-size: 1.25rem;
      font-weight: 800;
      line-height: 24px;

      @media (max-width: @tablet) {
        font-size: 1.125rem;
        line-height: 22px;
      }

      @media (max-width: @mobile) {
        font-size: 1rem;
        line-height: 20px;
      }
    }

    &__items {
      display: flex;
      flex-direction: column;
      gap: 6px;
      margin-left: 16px;

      @media (max-width: @tablet) {
        margin-left: 12px;
      }
    }

    &__item {
      font-size: 1rem;
      font-weight: 500;
      line-height: 20px;
      color: @color-text-second-black;

      @media (max-width: @tablet) {
        font-size: 0.9rem;
        line-height: 18px;
      }

      @media (max-width: @mobile) {
        font-size: 0.875rem;
        line-height: 16px;
      }
    }

    &__disclaimer {
      font-size: 0.75rem;
      font-weight: 700;
      line-height: 16px;
      color: @color-subtitle;
      margin-top: 24px;
      @media (min-width: @desktop) {
        padding: 0px 16px 16px 16px;
      }
    }

    &__link {
      text-decoration: underline;
      cursor: pointer;
    }
  }
  .matrix-transcription {
    background-color: @color-default-grey;
    padding: 16px;
    border-radius: 28px;
    display: flex;
    flex-direction: column;
    &__img {
      width: 100%;
      height: 100%;
      object-fit: contain;
    }
    &__title,
    &__description {
      @media (min-width: @desktop) {
        margin: 0 auto;
      }
    }
    &__title {
      margin-top: 24px;
      font-size: 1.5rem;
      font-weight: 900;
      line-height: 28px;
      text-align: center;

      @media (max-width: @laptop) {
        font-size: 1.375rem;
        line-height: 26px;
      }

      @media (max-width: @tablet) {
        font-size: 1.25rem;
        line-height: 24px;
      }

      @media (max-width: @mobile) {
        font-size: 1.25rem;
        line-height: 24px;
      }
    }

    &__description {
      margin-top: 12px;
      font-size: 1rem;
      font-weight: 700;
      line-height: 22px;
      text-align: center;
      color: @color-text-second-black;

      @media (max-width: @tablet) {
        font-size: 0.9rem;
        line-height: 20px;
      }

      @media (max-width: @mobile) {
        font-size: 0.875rem;
        line-height: 22px;
      }
    }
    &__button {
      margin-top: 24px;
      padding: 21px 0px;
      border-radius: 24px;
      border: 1px dashed @color-black-main;
      display: flex;
      align-items: center;
      justify-content: center;
      gap: 12px;

      @media (max-width: @tablet) {
        padding: 19px 0px;
        border-radius: 20px;
      }

      @media (max-width: @mobile) {
        padding: 17px 0px;
        border-radius: 16px;
      }

      &__icon {
        width: 24px;
        height: 24px;

        @media (max-width: @mobile) {
          width: 20px;
          height: 20px;
        }
      }

      &__text {
        font-size: 1.125rem;
        font-weight: 800;
        line-height: 20px;

        @media (max-width: @tablet) {
          font-size: 1rem;
          line-height: 18px;
        }

        @media (max-width: @mobile) {
          font-size: 1rem;
        }
      }

    }
  }
}
</style>
