<template>
  <ul class="resp-list" v-if="$store.state.languages == 'eng'">
    <li>
      Development of Web-app. Technology stack React.js, Next.js, gRPC, Node.js.
    </li>
  </ul>
  <ul class="resp-list" v-if="$store.state.languages == 'ru'">
    <li>
      Разработка Web-приложения мессенджера. Стек: React.js, Next.js, gRPC,
      Node.js.
    </li>
  </ul>
</template>

<script>
import store from "../../store";
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
