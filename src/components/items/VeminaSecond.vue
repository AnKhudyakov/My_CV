<template>
  <ul class="resp-list" v-if="$store.state.languages == 'eng'">
    <li>
      Participation in development of technical specification for interior of
      aircraft Il-96-400;
    </li>
    <li>Development of technical specifications for sub-contractors;</li>
    <li>
      Development nodes for interior of aircraft Il-96-400, preparation and
      design support of production;
    </li>
    <li>Interaction with the customer and sub-contractors;</li>
    <li>
      Ensuring deadlines and quality of documentation supplied to the customer.
    </li>
    <li>Ensuring an even load of engineers on the project.</li>
  </ul>
  <ul class="resp-list" v-if="$store.state.languages == 'ru'">
    <li>Участие в разработке ТЗ ОКР на интерьер самолёта Ил-96-400;</li>
    <li>Разработка Технического Задания для соисполнителей;</li>
    <li>
      Разработка узлов интерьера самолёта Ил-96-400 и сопровождение их
      изготовления на производстве;
    </li>
    <li>Взаимодействие с Заказчиком и подрядными организациями;</li>
    <li>
      Обеспечение сроков и качества конструкторской документации, соответствия
      ее нормам ЕСКД
    </li>
    <li>
      Обеспечение равномерной загрузки конструкторов, работающих на проекте.
    </li>
  </ul>
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
