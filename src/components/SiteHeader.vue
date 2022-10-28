<template>
  <div class="site-header mobile-hidden">
    <div class="logo-site">
      <Logo></Logo>
    </div>
    <MainMenu @newClick="Redirect"></MainMenu>
    <Languages></Languages>
  </div>
</template>

<script>
import Languages from './Languages.vue';
import MainMenu from './MainMenu.vue';
import Logo from './Logo.vue';
export default {
  components: {
    MainMenu,
    Logo,
    Languages,
  },
  methods: {
    Redirect() {
      this.$emit('newClick');
    },
  },
};
</script>

<style scoped>
.logo-site {
  display: flex;
  align-items: center;
  justify-content: center;
  width: 100%;
  height: 100px;
  padding: 5%;
}
.site-header {
  display: block;
  position: fixed;
  width: 160px;
  height: auto;
  top: 0;
  bottom: 0;
  padding: 10px 0 0;
  background-color: #fff;
  overflow: auto;
  z-index: 1002;
}
@media only screen and (max-width: 991px) {
  .mobile-hidden {
    display: none;
    visibility: hidden;
  }
}
</style>
