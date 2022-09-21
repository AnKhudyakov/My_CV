<template>
  <div class="item" v-for="item in items">
    <div class="left-part">
      <h4>{{ item.company }}</h4>
      <h5>{{ item.time }}</h5>
    </div>
    <div class="blank">
      <div class="line"></div>
    </div>
    <div class="right-part">
      <h4>{{ item.status }}</h4>
      <VeminaSecond v-if="item.resp === 'VeminaSecond'"></VeminaSecond>
      <VeminaFirst></VeminaFirst>
      <Progresstech></Progresstech>
      <Anotech v-if="item.resp === 'Anotech'"></Anotech>
    </div>
  </div>
</template>

<script>
import VeminaSecond from './items/VeminaSecond.vue';
import VeminaFirst from './items/VeminaFirst.vue';
import Progresstech from './items/Progresstech.vue';
import Anotech from './items/Anotech.vue';
export default {
  components: {
    VeminaSecond,
    VeminaFirst,
    Progresstech,
    Anotech,
  },
  props: {
    items: {
      type: Array,
    },
  },
};
</script>

<style scoped>
.item {
  display: grid;
  grid-template-columns: 1fr 0.5fr 2fr;
  margin-bottom: 15px;
}
.line {
  width: 50%;
  height: 100%;
  border-right: 3px solid #f5f5f5;
}
</style>
