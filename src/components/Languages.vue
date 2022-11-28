<template>
  <div class="languages">
    <div class="container_lang">
      <div v-if="$store.state.languages == 'ru'">
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

      <div v-if="$store.state.languages == 'eng'">
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
import Eng from "./icons/eng.vue";
import Ru from "./icons/ru.vue";
import store from "../store";
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
  width: fit-content;
  height: 50px;
  align-items: center;
  justify-content: center;
  margin-left: 35px;
}

.container_lang {
  display: flex;
  flex-direction: row;
  width: 100%;
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
