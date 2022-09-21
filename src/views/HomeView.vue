<script setup>
import Home from '../components/Home.vue';
import Main from '../components/Main.vue';
</script>

<template>
  <div class="main">
    <div class="avatar"></div>

    <div class="text-block">
      <Main msg="Андрей Худяков"> </Main>
    </div>
    <div class="changeable">
      <Home />
    </div>
  </div>
</template>

<style scoped>
.main {
  display: grid;
  background-color: #f5f5f5;
  grid-template-columns: 1fr 1fr;
  position: relative;
  width: 100%;
  height: 100%;
  z-index: 1001;
  overflow-y: auto;
}

.avatar {
  position: relative;
  background-image: url(../public/MyPhoto.JPG);
  height: 100%;
  min-height: 300px;
  width: 100%;
  background-position: top;
  background-size: cover;
  box-sizing: border-box;
  margin-left: 15px;
}

.text-block {
  padding: 70px 15%;
  background-color: #fcfcfc;
}
.changeable {
  background-color: #fff;
  grid-column: 1/3;
  position: relative;
  width: 100%;
  height: auto;
  margin-left: 15px;
  padding: 50px;
}

@media only screen and (max-width: 991px) {
  .avatar,
  .changeable {
    margin-left: 0;
  }
}
@media only screen and (max-width: 660px) {
  .main {
    display: flex;
    flex-direction: column;
  }
  .text-block {
    padding-bottom: 0;
  }
}
</style>
