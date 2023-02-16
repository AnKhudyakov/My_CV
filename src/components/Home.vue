<script>
import HomeItem from "./HomeItem.vue";
import EducationIcon from "./icons/IconEducation.vue";
import AboutIcon from "./icons/IconAbout.vue";
import store from "../store";
export default {
  data() {
    return {
      store,
    };
  },
  components: {
    HomeItem,
    EducationIcon,
    AboutIcon,
  },
};
</script>

<template>
  <h2 class="info-title" v-if="$store.state.languages == 'eng'">
    Personal information
  </h2>
  <h2 class="info-title" v-if="$store.state.languages == 'ru'">
    Личная информация
  </h2>
  <HomeItem v-if="$store.state.languages == 'eng'">
    <template #icon>
      <EducationIcon />
    </template>
    <template #heading>Education</template>

    2012 - Bauman Moscow State Technical University, faculty Power Engineering,
    speciality Rocket Engine Engineer.
    <a href="http://energo.bmstu.ru/e1/" target="_blank"> more </a>
  </HomeItem>

  <HomeItem v-if="$store.state.languages == 'ru'">
    <template #icon>
      <EducationIcon />
    </template>
    <template #heading>Образование</template>

    Высшее - В 2012г. закончил МГТУ им. Н.Э. Баумана, факультет Энергетическое
    машиностроение, по специальности Инженер-конструктор Ракетных Двигателей.
    <a href="http://energo.bmstu.ru/e1/" target="_blank">Подробнее</a>
  </HomeItem>

  <HomeItem v-if="$store.state.languages == 'eng'">
    <template #icon>
      <AboutIcon />
    </template>
    <template #heading>About Me</template>
    <p>
      I have experience in developing a multiservice web application on
      stack ReactJS, NextJS, Redux(Toolkit), gRPC, NodeJS, MongoDB. Also developed applications on MERN, PERN
      stacks with
      authorization via JWT/Google Sing In. I have experience with Strapi CMS, Stripe payment system, Material-UI
      library. I worked with AWS (EC2, RDS, S3) , Google Cloud Platform (App Engine, SQL,
      Storage). I know how to adapt, cross-browser layout.
    </p>
    <p>Changed pfofession due to a change of interests.</p>
    <p>
      Also i have the expirience of Senior Design Engineer: project and team (6
      persons) management, collection, analysis and structuring of customer
      requirements, development of technical specifications.
    </p>
  </HomeItem>

  <HomeItem v-if="$store.state.languages == 'ru'">
    <template #icon>
      <AboutIcon />
    </template>
    <template #heading>О себе</template>
    <p>
      Имею опыт разработки мультисервисного wеb-приложения на стеке ReactJS,
      NextJS, Redux(Toolkit), gRPC, NodeJS, MongoDB. Также разрабатывал
      приложения на стеках MERN, PERN с авторизацией по JWT/Google Sing In. Имею
      опыт работы с CMS Strapi, платежной системой Stripe, библиотекой Material-UI. Работал с AWS (EC2, RDS, S3) , Google Cloud Platform (App Engine, SQL,
      Storage). Умею адаптивно, кроссбраузерно верстать.
    </p>
    <p>Сменил сферу деятельности в связи со сменой интересов.</p>
    <p>
      Также имею опыт главного специалиста конструкторского отдела: ведение
      проектов, управление командой проекта (6 человек), сбор, анализ и
      структурирование требований заказчика, разработка ТЗ, решение
      организационных и административных вопросов.
    </p>
  </HomeItem>
</template>

<style scoped>
.info-title {
  width: fit-content;
  border-bottom: 2px solid #017796;
}
</style>
