<template>
  <nav>
    <ul class="site-main-menu">
      <li v-bind:class="ActiveAbout" @click="ActiveCurrent">
        <RouterLink to="/" v-if="$store.state.languages == 'eng'"
          >About Me</RouterLink
        >
        <RouterLink to="/" v-if="$store.state.languages == 'ru'"
          >Обо мне</RouterLink
        >
      </li>
      <li v-bind:class="ActiveResume" @click="ActiveCurrent">
        <RouterLink to="/resume" v-if="$store.state.languages == 'eng'"
          >Resume</RouterLink
        >
        <RouterLink to="/resume" v-if="$store.state.languages == 'ru'"
          >Резюме</RouterLink
        >
      </li>
      <li v-bind:class="ActiveContacts" @click="ActiveCurrent">
        <RouterLink to="/contacts" v-if="$store.state.languages == 'eng'"
          >Contacts</RouterLink
        >
        <RouterLink to="/contacts" v-if="$store.state.languages == 'ru'"
          >Контакты</RouterLink
        >
      </li>
    </ul>
  </nav>
</template>

<script>
import store from '../store';
export default {
  data() {
    return {
      ActiveResume: '',
      ActiveAbout: 'active',
      ActiveContacts: '',
      store,
    };
  },
  methods: {
    ActiveCurrent(event) {
      if (
        event.target.innerHTML === 'About Me' ||
        event.target.innerHTML === 'Обо мне'
      ) {
        this.ActiveAbout = 'active';
        this.ActiveResume = '';
        this.ActiveContacts = '';
      } else if (
        event.target.innerHTML === 'Contacts' ||
        event.target.innerHTML === 'Контакты'
      ) {
        this.ActiveContacts = 'active';
        this.ActiveResume = '';
        this.ActiveAbout = '';
      } else if (
        event.target.innerHTML === 'Resume' ||
        event.target.innerHTML === 'Резюме'
      ) {
        this.ActiveResume = 'active';
        this.ActiveContacts = '';
        this.ActiveAbout = '';
      }
    },
  },
};
</script>

<style scoped>
nav {
  display: block;
  width: 100%;
  text-align: center;
  padding: 25px 0 25px;
}

nav a.router-link-exact-active {
  color: var(--color-text);
}

nav a.router-link-exact-active:hover {
  background-color: transparent;
}
</style>
