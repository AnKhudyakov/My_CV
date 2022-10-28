<template>
  <div class="languages">
    <div class="container_lang">
      <div>
        <a
          class="row"
          href="#"
          role="button"
          @click="$store.state.languages = 'eng'"
        >
          <Eng class="en"></Eng>
          <div>English</div>
        </a>
      </div>

      <div>
        <a
          class="row"
          href="#"
          role="button"
          @click="$store.state.languages = 'ru'"
        >
          <Ru class="ru"></Ru>
          <div>Русский</div>
        </a>
      </div>
    </div>
  </div>
</template>

<script>
import Eng from './icons/eng.vue';
import Ru from './icons/ru.vue';
import store from '../store';
export default {
  data() {
    return {
      store,
    };
  },

  components: {
    Eng,
    Ru,
  },
};
</script>

<style scoped>
.languages {
  display: flex;
  flex-direction: column;
  width: 100%;
  height: 50px;
  align-items: flex-end;
  justify-content: center;
}

.container_lang {
  display: flex;
  flex-direction: row;
  width: fit-content;
  height: fit-content;
  justify-content: center;
  align-items: center;
}
.row {
  display: flex;
  flex-direction: row;
  width: fit-content;
  justify-items: flex-end;
  align-items: flex-end;
  padding: 0 5px 0 5px;
}

.en,
.ru {
  scale: 0.7;
}
/*
@media only screen and (max-width: 991px) {
  .languages {
    display: flex;
    flex-direction: row;
    align-items: center;
    width: fit-content;
  }
}*/
</style>
