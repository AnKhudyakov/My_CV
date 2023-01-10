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
      <Sfera v-if="item.resp === 'Sfera'"></Sfera>
      <VeminaSecond v-if="item.resp === 'VeminaSecond'"></VeminaSecond>
      <VeminaFirst v-if="item.resp === 'VeminaFirst'"></VeminaFirst>
      <Progresstech v-if="item.resp === 'Progresstech'"></Progresstech>
      <Anotech v-if="item.resp === 'Anotech'"></Anotech>
    </div>
  </div>
</template>

<script>
import VeminaSecond from "./items/VeminaSecond.vue";
import VeminaFirst from "./items/VeminaFirst.vue";
import Progresstech from "./items/Progresstech.vue";
import Anotech from "./items/Anotech.vue";
import Sfera from "./items/Sfera.vue";
export default {
  components: {
    VeminaSecond,
    VeminaFirst,
    Progresstech,
    Anotech,
    Sfera,
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
  grid-template-columns: 1fr 0.1fr 2fr;
  margin-bottom: 15px;
  height: fit-content;
}
.line {
  width: 50%;
  height: 100%;
  border-right: 3px solid #f5f5f5;
}
.right-part {
  padding: 0 10px 0 20px;
  overflow-y: none;
}
.blank {
  margin: 0 5px 0 5px;
}
.left-part {
  min-width: 125px;
}
</style>
