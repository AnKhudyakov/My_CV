<template>
  <div class="page-resume">
    <div class="resume">
      <div class="section-title">
        <h2 v-if="$store.state.languages == 'eng'">Resume</h2>
        <h2 v-if="$store.state.languages == 'ru'">Резюме</h2>
      </div>
      <div class="main-section">
        <div class="expirience">
          <div class="block-title">
            <h3 v-if="$store.state.languages == 'eng'">Experience</h3>
            <h3 v-if="$store.state.languages == 'ru'">Опыт работы</h3>
          </div>
          <div class="content">
            <ResumeItem
              v-if="$store.state.languages == 'eng'"
              :items="items"
            ></ResumeItem>
            <ResumeItem
              v-if="$store.state.languages == 'ru'"
              :items="itemsRu"
            ></ResumeItem>
          </div>
        </div>
        <div class="skills">
          <div class="block-title">
            <h3 v-if="$store.state.languages == 'eng'">Skills</h3>
            <h3 v-if="$store.state.languages == 'ru'">Ключевые навыки</h3>
          </div>
          <div class="content-skills">
            <SkillsItem :skills="skills"></SkillsItem>
          </div>
          <div class="block-title">
            <h3 v-if="$store.state.languages == 'eng'">Foreign languages</h3>
            <h3 v-if="$store.state.languages == 'ru'">Иностранные языки</h3>
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
import store from '../store';
export default {
  components: {
    ResumeItem,
    SkillsItem,
  },
  data() {
    return {
      items: [
        {
          company: '"Vemina Aviaprestige"',
          time: 'April 19 - January 20',
          status: 'Senior Design Engineer',
          resp: 'VeminaSecond',
        },
        {
          company: '"Anotech Energy"',
          time: 'May 18 - March 19',
          status: 'Lead Design Engineer',
          resp: 'Anotech',
        },
        {
          company: '"Vemina Aviaprestige"',
          time: 'April 13 - May 18',
          status: 'Design Engineer',
          resp: 'VeminaFirst',
        },
        {
          company: '"Progresstech"',
          time: 'January 12 - April 13',
          status: 'Design Engineer',
          resp: 'Progresstech',
        },
      ],
      itemsRu: [
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
      languages: [{ name: 'English', percentage: 'skill-60' }],
      store,
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
  overflow-x: hidden;
}
.resume {
  position: relative;
  padding: 50px;
  width: 100%;
  height: fit-content;
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
  .resume {
    padding: 30px;
  }
}
</style>
