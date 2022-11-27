<script>
import store from "../store";
export default {
  data() {
    return {
      store,
    };
  },
  props: {
    msg: {
      type: String,
      required: true,
    },
  },
};
</script>

<template>
  <div class="greetings">
    <h2 class="main-title">{{ msg }}</h2>
    <h4 v-if="$store.state.languages == 'eng'">Front-End Developer</h4>
    <p v-if="$store.state.languages == 'eng'">
      Front-End Developer with a proven ability to adapt in both self-starting
      and collaborative environments while staying focused on achieving
      high-quality resultsunder strict deadlines. My technology stack: React.js,
      Redux, Next.js, Vue.js, JavaScript, HTML5, CSS, SCSS.
    </p>
    <h4 v-if="$store.state.languages == 'ru'">Front-End разработчик</h4>
    <p v-if="$store.state.languages == 'ru'">
      Front-End разработчик с способностью адаптироваться к среде как
      самостоятельной, так и совместной работы на проекте, сохраняя при этом
      сосредоточенность на достижении высококачественных результатов в сжатые
      сроки. Мой стек технологий: React.js, Redux, Next.js, Vue.js, JavaScript,
      HTML5, CSS, SCSS.
    </p>
  </div>
</template>

<style scoped>
.main-title {
  font-size: 48px;
  line-height: 1.2em;
  margin-bottom: 15px;
  text-align: justify;
}

.greetings p {
  margin-top: 5px;
}

@media (min-width: 1024px) {
  .greetings h1 {
    text-align: left;
  }
}
</style>
