<template>
  <div class="page-resume">
    <div class="resume">
      <div class="section-title">
        <h2>Резюме</h2>
      </div>
      <div class="main-section">
        <div class="expirience">
          <div class="block-title">
            <h3>Опыт работы</h3>
          </div>
          <div class="content">
            <ResumeItem :items="items"></ResumeItem>
          </div>
        </div>
        <div class="skills">
          <div class="block-title">
            <h3>Ключевые навыки</h3>
          </div>
          <div class="content-skills">
            <SkillsItem :skills="skills"></SkillsItem>
          </div>
          <div class="block-title">
            <h3>Иностранные языки</h3>
          </div>
          <div class="content-skills">
            <SkillsItem :skills="languages"></SkillsItem>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import ResumeItem from '../components/ResumeItem.vue';
import SkillsItem from '../components/SkillsItem.vue';
export default {
  components: {
    ResumeItem,
    SkillsItem,
  },
  data() {
    return {
      items: [
        {
          company: 'ООО "Вемина Авиапрестиж"',
          time: 'Апрель 19 - Январь 20',
          status: 'Главный специалист кострукторского отдела',
          resp: 'VeminaSecond',
        },
        {
          company: 'АО "Anotech Energy"',
          time: 'Май 18 - Март 19',
          status: 'Ведущий инженер-конструктор',
          resp: 'Anotech',
        },
        {
          company: 'ООО "Вемина Авиапрестиж"',
          time: 'Апрель 13 - Май 18',
          status: 'Инженер-конструктор',
          resp: 'VeminaFirst',
        },
        {
          company: 'АО "Прогресстех""',
          time: 'Июнь 12 - Апрель 13',
          status: 'Инженер-конструктор',
          resp: 'Progresstech',
        },
      ],
      skills: [
        { name: 'HTML5, CSS', percentage: 'skill-80' },
        { name: 'JavaScript(ES6)', percentage: 'skill-70' },
        { name: 'Vue.js', percentage: 'skill-60' },
        { name: 'Git', percentage: 'skill-80' },
        { name: 'SQL', percentage: 'skill-90' },
      ],
      languages: [{ name: 'Английский', percentage: 'skill-60' }],
    };
  },
};
</script>

<style scoped>
.page-resume {
  width: 100%;
  height: 100%;
  background-color: #f5f5f5;
  overflow-y: auto;
}
.resume {
  position: relative;
  padding: 50px;
  width: 100%;
  height: 100%;
  margin-left: 15px;
  background-color: #fff;
}
.section-title {
  border-bottom: 3px solid #f5f5f5;
}

.main-section {
  display: grid;
  grid-template-columns: 2fr 1fr;
  margin-top: 15px;
}
.content-skills {
  margin-bottom: 15px;
}

.block-title h3 {
  width: fit-content;
  margin-bottom: 20px;
  border-bottom: 2px solid #017796;
}

@media only screen and (max-width: 991px) {
  .resume {
    margin-left: 0;
  }
}
@media (max-width: 750px) {
  .main-section {
    min-height: 100vh;
    display: flex;
    flex-direction: column;
  }
}
</style>
