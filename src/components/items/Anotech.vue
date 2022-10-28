<template>
  <div v-if="$store.state.languages == 'eng'">
    <h5>Like a Team Leader:</h5>
    <ul class="resp-list">
      <li>Recruitment and management of the project team;</li>
      <li>
        Interaction with the customer(collection, analysis and structuring of
        customer requirements);
      </li>
      <li>Time and resource estimation of the tasks;</li>
      <li>Mentoring new employees;</li>
      <li>Quality control of documentation supplied to the customer</li>
    </ul>
    <h5>Like a Design Engineer:</h5>
    <ul class="resp-list">
      <li>
        Development of the secondary structure of the Airbus А320 aircraft
        family. Preparing a documentation package.
      </li>
    </ul>
  </div>
  <div v-if="$store.state.languages == 'ru'">
    <h5>Как руководитель проекта:</h5>
    <ul class="resp-list">
      <li>Набор и управление командой проекта;</li>
      <li>
        Взаимодействие с Заказчиком(сбор, анализ и структурирование требований
        заказчика)
      </li>
      <li>
        Оценка загрузки на проекте и трудоемкости текущей проектной работы;
      </li>
      <li>
        Оценка рисков, связанных с проектированием и предложение плана чтобы
        уменьшить или избежать негативного воздействия;
      </li>
      <li>Наставничество новичков;</li>
      <li>Решение всех организационных и административных вопросов;</li>
      <li>Контроль полноты и качества поставляемой Заказчику документации</li>
    </ul>
    <h5>Как инженер конструктор:</h5>
    <ul class="resp-list">
      <li>
        Проектная деятельность по вторичной структуре семейства самолётов Airbus
        А320. Подготовка пакета документов.
      </li>
    </ul>
  </div>
</template>

<script>
import store from '../../store';
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
