<template>
  <div class="mobile-header mobile-visible">
    <div class="contain-mobile-header">
      <div class="logo-mobile">
        <Logo class="logo-img"></Logo>
      </div>
      <div class="lang">
        <Languages></Languages>
      </div>

      <div class="mobile-menu">
        <a
          class="link"
          href="#"
          role="button"
          data-bs-toggle="dropdown"
          aria-expanded="false"
          @click="$store.state.show = !$store.state.show"
        >
          <img src="../assets/list.svg" alt="list" class="menu-toggle" />
        </a>
        <Transition name="slide-siteHeader">
          <SiteHeader
            class="show-siteHeader"
            @click="$store.state.show = !$store.state.show"
            v-show="$store.state.show"
          ></SiteHeader>
        </Transition>
      </div>
    </div>
  </div>
</template>

<script>
import Logo from "./Logo.vue";
import SiteHeader from "./SiteHeader.vue";
import Languages from "./Languages.vue";
import store from "../store";
export default {
  components: {
    SiteHeader,
    Logo,
    Languages,
  },
  data() {
    return {
      store,
      ChangeClass: "hide-siteHeader",
    };
  },
};
</script>

<style scoped>
.show-siteHeader {
  display: block;
  position: fixed;
  width: 100%;
  max-width: 160px;
  height: calc(100%-50px);
  top: 50px;
  left: 0;
  overflow: auto;
  box-shadow: 0 0 10px 0 rgb(0 0 0 / 18%);
  z-index: 1001;
  visibility: visible;
}

.mobile-header {
  display: none;
  visibility: hidden;
}
.contain-mobile-header {
  display: flex;
  flex-direction: row;
  height: 100%;
  width: 100%;
}

.mobile-menu .logo-mobile {
  display: flex;
  align-content: center;
  justify-items: center;
  width: 85px;
  height: 100%;
}

.lang {
  width: 100%;
  display: flex;
  justify-content: flex-end;
}

.link,
.menu-toggle {
  width: 100%;
  height: 100%;
  padding: 0;
}
.slide-siteHeader-enter-active {
  transition: all 0.5s ease-out;
  animation-direction: reverse;
}

.slide-siteHeader-leave-active {
  transition: all 0.5s ease-in;
}

.slide-siteHeader-enter-from,
.slide-siteHeader-leave-to {
  transform: translateX(-20px);
  opacity: 0;
}
@media only screen and (max-width: 991px) {
  .mobile-header {
    position: fixed;
    display: inline-block;
    width: 100%;
    max-width: 100%;
    background-color: #fff;
    border-bottom: 1px solid #f5f5f5;
    top: 0;
    left: 0;
    right: 0;
    height: 50px;
    z-index: 1002;
  }

  .mobile-visible {
    display: block;
    visibility: visible;
  }
}
</style>
