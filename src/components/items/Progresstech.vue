<template>
  <ul class="resp-list" v-if="$store.state.languages == 'eng'">
    <li>
      Development of documentation and 3D models for Boeing 737,767,777 aircraft
      nodes;
    </li>
    <li>Participation in serial production support for this aircraft family</li>
  </ul>
  <ul class="resp-list" v-if="$store.state.languages == 'ru'">
    <li>
      Разработка конструкторской документации и трехмерных моделей на узлы
      самолетов Boeing 737,767,777;
    </li>
    <li>
      Участие в поддержке серийного производства для данного семейства самолетов
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
