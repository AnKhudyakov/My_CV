<template>
  <ul class="resp-list" v-if="$store.state.languages == 'eng'">
    <li>
      РDevelopment of documentation and 3D models for vip-interior of aircrafts:
      Il-96-300, RRJ-95, Tu-204, Tu-214 and helicopters Mi8
    </li>
    <li>Stress analysis estimation</li>
    <li>Design support of production</li>
  </ul>
  <ul class="resp-list" v-if="$store.state.languages == 'ru'">
    <li>
      Разработка конструкторской документации и трехмерных моделей на
      vip-интерьеры самолетов Ил-96-300, RRJ-95, Ту-204, Ту-214 и вертолетов Ми8
    </li>
    <li>Проведение оценочных прочностных расчетов силовых элементов</li>
    <li>Конструкторское сопровождение производства</li>
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
