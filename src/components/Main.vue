<script setup>
defineProps({
  msg: {
    type: String,
    required: true,
  },
});
</script>

<template>
  <div class="greetings">
    <h2 class="main-title">{{ msg }}</h2>
    <p>Frontend-разработчик(junior)</p>
    <p>Занятость: Полная</p>
    <p>График работы: Полный день</p>
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
