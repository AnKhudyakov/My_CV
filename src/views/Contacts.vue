<template>
  <div class="page-contacts">
    <div class="contacts">
      <h2 v-show="$store.state.languages == 'eng'">Contacts</h2>
      <h2 v-show="$store.state.languages == 'ru'">Контакты</h2>
    </div>
    <div class="mail">
      <a href="mailto:khandrewv@gmail.com" target="_blank">
        <div class="lm-info-block">
          <i>
            <img src="../assets/envelope.svg" alt="envelope" class="envelope" />
          </i>
          <h4>khandrewv@gmail.com</h4>
        </div>
      </a>
    </div>
    <div class="phone">
      <a href="tel:+79269264898" target="_blank">
        <div class="lm-info-block">
          <i>
            <img
              src="../assets/telephone.svg"
              alt="envelope"
              class="envelope"
            />
          </i>
          <h4>+7 (926) 926-48-98</h4>
        </div>
      </a>
    </div>
  </div>
</template>

<script>
import store from '../store';
export default {
  data() {
    return {
      store,
    };
  },
};
</script>

<style scoped>
.page-contacts {
  margin-left: 15px;
  padding: 50px;
  width: 100%;
  height: 100%;
  background-color: #fff;
}
.contacts {
  border-bottom: 3px solid #f5f5f5;
}
.mail .phone {
  position: relative;
  width: 100%;
  padding: 0 15px 30px 15px;
}
.lm-info-block {
  position: relative;
  text-align: center;
  width: 100%;
  display: block;
  margin-top: 20px;
  background: #fff;
  padding: 20px 10px 15px;
  border: 1px solid #eee;
  -webkit-box-shadow: none;
  -moz-box-shadow: none;
  box-shadow: none;
  overflow: hidden;
  -webkit-transition: all 0.2s ease-in-out;
  -moz-transition: all 0.2s ease-in-out;
  -o-transition: all 0.2s ease-in-out;
  -ms-transition: all 0.2s ease-in-out;
  transition: all 0.2s ease-in-out;
}
.lm-info-block i {
  position: relative;
  font-size: 40px;
  color: #b5b5b5;
}

.lm-info-block h4 {
  font-size: 16px;
  margin-top: 20px;
}
.envelope {
  scale: 2.5;
}
@media only screen and (max-width: 991px) {
  .page-contacts {
    margin-left: 0;
  }
}
</style>
