<script setup>
import HomeItem from './HomeItem.vue';
import EducationIcon from './icons/IconEducation.vue';
import AboutIcon from './icons/IconAbout.vue';
</script>

<template>
  <h2 class="info-title">Личная информация</h2>
  <HomeItem>
    <template #icon>
      <EducationIcon />
    </template>
    <template #heading>Образование</template>

    Высшее - В 2012г. закончил МГТУ им. Н.Э. Баумана, факультет Энергетическое
    машиностроение, по специальности Инженер-конструктор Ракетных Двигателей.
    <a href="http://energo.bmstu.ru/e1/" target="_blank">Подробнее</a>
  </HomeItem>

  <HomeItem>
    <template #icon>
      <AboutIcon />
    </template>
    <template #heading>О себе</template>
    <p>
      Сменил сферу деятельности в связи со сменой интересов и ограничением в
      развитии в инженерной сфере.
    </p>
    <p>
      Имею опыт главного специалиста конструкторского отдела: ведение проектов,
      управление командой проекта (6 человек), сбор, анализ и структурирование
      требований заказчика, разработка ТЗ, решение организационных и
      административных вопросов.
    </p>
  </HomeItem>
</template>

<style scoped>
.info-title {
  width: fit-content;
  border-bottom: 2px solid #017796;
}
</style>
