<script setup lang="ts">
import { ref } from "vue";
import MatrixSlot from "./MatrixSlot.vue";
import AboutDropContent from "./AboutDropContent.vue";
import AboutDropHeader from "./AboutDropHeader.vue";
import PromotionBlock from "./PromotionBlock.vue";

const isFirstContentVisible = ref(true);
const isSecondContentVisible = ref(true);

const toggleFirstContent = () => {
  isFirstContentVisible.value = !isFirstContentVisible.value;
};

const toggleSecondContent = () => {
  isSecondContentVisible.value = !isSecondContentVisible.value;
};
</script>

<template>
  <div class="matrix-about">
    <h2 class="matrix-about__title">1. Общая информация</h2>
    <div class="matrix-about__drop">
      <AboutDropHeader
        :is-open="isFirstContentVisible"
        @toggle="toggleFirstContent"
        title="Личные качества"
        description="Плюсы и минусы"
        img="/src/assets/mirror-girl.svg"
      />
      <transition name="fade">
        <AboutDropContent
          v-if="isFirstContentVisible"
          title="Визитная карточка: характер человека в плюсе и минусе"
          description="Это своего рода, «визитная карточка»: характер и личные качества, которые человек получает в момент рождения. Как и всё другое в Матрице судьбы, этот аспект имеет как положительный, так и отрицательный вариант развития. Хотя на практике плюсы и минусы находятся в некой неравной пропорции. Соответственно, положительные моменты нужно развивать, а отрицательные прорабатывать или, как минимум знать о них, и стараться нивелировать."
        />
      </transition>
    </div>
    <div class="matrix-about__drop">
      <AboutDropHeader
        :is-open="isSecondContentVisible"
        @toggle="toggleSecondContent"
        title="Кармический хвост"
        description="Задачи прошлой жизни"
        img="/src/assets/Кармический хвост.svg"
      />
      <transition name="fade">
        <AboutDropContent
          v-if="isSecondContentVisible"
          title="Кармический хвост или задачи прошлой жизни"
          description="Кармическая программа, или как её ещё называют «кармический хвост» по Матрице судьбы — это то, с чем душа не успела, не смогла или не захотела справиться в своём прошлом воплощении. Обычно это первое, с чего следует начинать проработку своей матрицы после первого знакомства. Постарайтесь понять, какие ошибки вы допустили в предыдущей жизни, и что вам нужно сделать в нынешней… "
        />
      </transition>
    </div>
    <div class="matrix-about__slot">
      <MatrixSlot
        title="Проработка души"
        description="В нынешнем воплощении"
        img="/src/assets/Проработка души.svg"
      />
      <MatrixSlot
        title="Главные задачи души"
        description="До 40 лет"
        img="/src/assets/Главные задачи души до 40 лет.svg"
      />
      <MatrixSlot
        title="Точка гармонии"
        description="и душевный комфорт"
        img="/src/assets/Точка гармонии.svg"
      />
      <MatrixSlot
        title="Родовые программы"
        description="По линии отца и матери"
        img="/src/assets/Родовые программы по линии отца и матери.svg"
      />
      <MatrixSlot
        title="Врождённые таланты"
        description="человека"
        img="/src/assets/Врожденные таланты.svg"
      />
      <MatrixSlot
        title="Детско-родительская"
        description="карма"
        img="/src/assets/Детско-родительская карма.svg"
      />
      <MatrixSlot
        title="Личное"
        description="предназначение человека"
        img="/src/assets/Личное предназначение человека.svg"
      />
      <MatrixSlot
        title="Социальное"
        description="предназначение человека"
        img="/src/assets/Социальное предназначение.svg"
      />
      <MatrixSlot
        title="Духовное"
        description="предназначение человека"
        img="/src/assets/Духовное предназначение.svg"
      />
      <MatrixSlot
        title="Встреча"
        description="и готовность к отношениям"
        img="/src/assets/Встреча и готовность к отношениям.svg"
      />
      <MatrixSlot
        title="Общий характер"
        description="отношений с партнёром"
        img="/src/assets/Общий характер отношений с партнером.svg"
      />
      <MatrixSlot
        title="Общее состояние"
        description="и кармические задачи"
        img="/src/assets/Общее состояние и кармические задачи.svg"
      />
      <MatrixSlot
        title="Финансовый потенциал"
        description="и профессии"
        img="/src/assets/Финансовый потенциал и профессии.svg"
      />
      <MatrixSlot
        title="Денежный поток"
        description="блок и развитие"
        img="/src/assets/Денежный поток блокировка и развитие.svg"
      />
      <MatrixSlot
        title="Чакровая карта"
        description="здоровья"
        img="/src/assets/Чакровая карта здоровья.svg"
      />
      <MatrixSlot
        title="Прогноз"
        description="по годам жизни"
        img="/src/assets/Прогноз по годам жизни.svg"
      />
      <PromotionBlock />
    </div>
  </div>
</template>

<style lang="less" scoped>
@import "../styles/variables.less";
.matrix-about {
  display: flex;
  flex-direction: column;
  max-width: 932px;

  @media (max-width: @laptop) {
    max-width: 100%;
  }

  @media (max-width: @tablet) {
    max-width: 100%;
  }

  @media (max-width: @mobile) {
    max-width: 100%;
  }

  &__slot {
    display: flex;
    flex-direction: column;
    gap: 14px;
    @media (max-width: @mobile) {
      margin: 0px 8px;
    }
  }

  &__title {
    font-size: 2rem;
    font-weight: 900;
    line-height: 40px;
    margin-bottom: 32px;

    @media (max-width: @laptop) {
      font-size: 1.75rem;
      line-height: 36px;
      margin-bottom: 28px;
    }

    @media (max-width: @tablet) {
      font-size: 1.5rem;
      line-height: 32px;
      margin-bottom: 24px;
    }

    @media (max-width: @mobile) {
      font-size: 1.75rem;
      line-height: 32px;
      margin-bottom: 20px;
    }
  }

  &__drop {
    border-radius: 44px;
    border: 1px solid rgba(236, 236, 236, 1);
    display: flex;
    flex-direction: column;
    gap: 16px;
    overflow: hidden;
    transition: all 0.3s ease;

    @media (max-width: @tablet) {
      border-radius: 32px;
      gap: 12px;
    }

    @media (max-width: @mobile) {
      border-radius: 0px;
      border: none;
      gap: 8px;
    }
  }
}

.fade-enter-active,
.fade-leave-active {
  transition: opacity 0.3s ease;
}

.fade-enter-from,
.fade-leave-to {
  opacity: 0;
}
</style>
