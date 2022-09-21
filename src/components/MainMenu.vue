<template>
  <nav>
    <ul class="site-main-menu">
      <li v-bind:class="ActiveAbout" @click="ActiveCurrent">
        <RouterLink to="/">Обо мне</RouterLink>
      </li>
      <li v-bind:class="ActiveResume" @click="ActiveCurrent">
        <RouterLink to="/resume">Резюме</RouterLink>
      </li>
      <li v-bind:class="ActiveContacts" @click="ActiveCurrent">
        <RouterLink to="/contacts">Контакты</RouterLink>
      </li>
    </ul>
  </nav>
</template>

<script>
export default {
  data() {
    return {
      ActiveResume: '',
      ActiveAbout: 'active',
      ActiveContacts: '',
    };
  },
  methods: {
    ActiveCurrent(event) {
      if (event.target.innerHTML === 'Обо мне') {
        this.ActiveAbout = 'active';
        this.ActiveResume = '';
        this.ActiveContacts = '';
      } else if (event.target.innerHTML === 'Контакты') {
        this.ActiveContacts = 'active';
        this.ActiveResume = '';
        this.ActiveAbout = '';
      } else if (event.target.innerHTML === 'Резюме') {
        this.ActiveResume = 'active';
        this.ActiveContacts = '';
        this.ActiveAbout = '';
      }
      this.$emit('newClick');
    },
  },
};
</script>

<style scoped>
nav {
  display: block;
  width: 100%;
  text-align: center;
  padding: 25px 0 40px;
}

nav a.router-link-exact-active {
  color: var(--color-text);
}

nav a.router-link-exact-active:hover {
  background-color: transparent;
}
</style>
