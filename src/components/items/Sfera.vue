<template>
  <ul class="resp-list" v-if="$store.state.languages == 'eng'">
    <li>
      Development of microservices social-network Web-app . Technology stack
      ReactJS, NextJS, Redux(Toolkit), gRPC, NodeJS, MongoDB;
    </li>
    <li>Development and implementation of new interfaces and functionality;</li>
    <li>Optimization and maintenance of existing code, fixing bugs;</li>
    <li>Participation in the development of the application architecture;</li>
    <li>Estimation and decomposition of tasks for the project;</li>
    <li>Crossbrowser layout;</li>
    <li>Unit and integration testing.</li>
  </ul>
  <ul class="resp-list" v-if="$store.state.languages == 'ru'">
    <li>
      Разработка микросервисного Web-приложения социальной сети. Технологический
      стек: ReactJS, NextJS, Redux(Toolkit), gRPC, NodeJS, MongoDB;
    </li>
    <li>Проработка и реализация новых интерфейсов и функционала;</li>
    <li>Оптимизация и поддержание существующего кода, исправление багов;</li>
    <li>Участие в развитии архитектуры приложения;</li>
    <li>Оценка и декомпозиция задач по проекту;</li>
    <li>Кроссбраузерная вёрстка;</li>
    <li>Unit и интеграционное тестирование.</li>
  </ul>
</template>

<script>
import store from "../../store";
export default {
  data() {
    return {
      store,
    };
  },
};
</script>

<style scoped>
.resp-list li {
  list-style-type: circle;
}
</style>
