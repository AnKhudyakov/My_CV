<template>
  <div class="skill-List" v-for="skill in skills">
    <div class="skill-name">
      {{ skill.name }}
    </div>
    <div class="skill-container">
      <div :class="skillsPercent(skill.percentage)"></div>
    </div>
  </div>
</template>

<script>
export default {
  methods: {
    skillsPercent(percentage) {
      const classPercent = `skill-percentage + ${percentage}`;
      return classPercent;
    },
  },
  props: {
    skills: {
      type: Array,
    },
  },
};
</script>

<style scoped>
.skill-container {
  position: relative;
  background-color: transparent;
  border: 1px solid #017796;
  -moz-border-radius: 8px;
  -webkit-border-radius: 8px;
  border-radius: 8px;
  -webkit-box-sizing: border-box;
  -moz-box-sizing: border-box;
  box-sizing: border-box;
  height: 10px;
  margin-bottom: 15px;
  width: 100%;
}

.skill-percentage {
  background-color: #017796;
  border: 2px solid #fff;
  -moz-border-radius: 9px;
  -webkit-border-radius: 9px;
  border-radius: 9px;
  height: 8px;
  padding: 0;
}
.skill-60 {
  width: 60%;
}
.skill-70 {
  width: 70%;
}
.skill-80 {
  width: 80%;
}
.skill-90 {
  width: 90%;
}
</style>
