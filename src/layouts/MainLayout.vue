<template>
  <!DOCTYPE html>
  <html>
    <header>
      <div class="q-pa-md">
        <q-toolbar class="bg-black text-white shadow-2 rounded-borders">
          <q-btn class="tabs" flat label="Mohammad Odah" />
          <q-space />

          <!--
        notice shrink property since we are placing it
        as child of QToolbar
      -->
          <q-tabs v-model="tab" shrink stretch>
            <q-route-tab
              class="tabs"
              name="tab1"
              href="https://github.com/moeodah"
              icon="eva-github-outline"
            />
            <q-route-tab class="tabs" name="tab1" icon="eva-twitter-outline" />
            <q-route-tab
              class="tabs"
              name="tab2"
              href="https://www.linkedin.com/in/mohammad-o-0abab089/"
              icon="eva-linkedin-outline"
            />
          </q-tabs>
        </q-toolbar>
      </div>
    </header>
    <body>
      <div class="row">
        <div class="col-sm-2 float-left">
          <q-btn class="join" icon="eva-home-outline"> H O M E </q-btn>
          <q-btn class="join" icon="eva-info-outline">O D A H</q-btn>
          <q-btn class="join" icon="eva-briefcase-outline">W O R K</q-btn>
          <q-btn class="join" icon="eva-email-outline">F I N D ME</q-btn>
        </div>
        <nav class="menu">
          <q-btn
            v-if="button"
            icon="eva-power-outline"
            @click="change(this)"
            class="myIcon"
          />
          <q-btn
            v-if="!button"
            icon="eva-close-circle-outline"
            @click="change()"
            class="myIconclose"
          />
          <q-btn v-if="!button" icon="eva-book-open-outline" class="git" />
          <q-btn v-if="!button" icon="eva-globe-2-outline" class="twitter" />
          <q-btn v-if="!button" icon="eva-phone-outline" class="linkedin" />
        </nav>
      </div>
    </body>
  </html>
</template>
<script>
import { ref } from 'vue';

export default {
  setup() {
    var button = ref([]);
    function change() {
      button.value = !button.value;
      console.log(button.value);
    }
    return {
      change,
      button,
      slide: ref('style'),
      lorem:
        //' Great to meet you, My Name is Mohammad Odah, I am a Computer Science Graduate, I am from Ottawa Canada',
        'moe moe moe',
      school: 'I have graduated from Carleton University in Ottawa',
      passion:
        'I am trying to become a full fledged full stack developer. Currently I am trying to perfect Vue.js while working with react & I am working on perfecting my skills in IOS development ',
      future:
        'I am hoping that I will be able to start my own company of web and mobile development ',
    };
  },
};
</script>
<style >
body,
h1 {
  font-family: 'Montserrat', sans-serif;
  color: aliceblue;
}
body {
  background: black;
  background-size: auto;

  /* background-image: url('../assets/black.png'); */
}
.main {
  width: 700px;
  flex: none;
  position: relative;
  top: 0%;
  left: 55%;
}
.main2 {
  flex: none;
}
.mainBody {
  width: auto;
  flex: none;
  position: relative;
  top: 400px;
  left: 0px;
}
.tabs {
  transition: 0.3s;
  background: none;
  color: lightcyan;
  outline: none;
}
.tabs:hover {
  transition: 0.3;
  background: lightcyan;
  color: black;
}
.join {
  transition: 0.3s;
  width: 110px;
  height: 110px;
  background: none;
  font-size: 15px;
  color: lightcyan;
  outline: none;
  border-radius: 60px;
  cursor: pointer;
  position: relative;
  margin: 20px;
}
.join:hover {
  transition: 0.3;
  background: lightcyan;
  border-radius: 60px;
  color: black;
  box-shadow: 0px 0px 40px lightcyan;
}

.myIcon {
  position: fixed;
  margin-top: -50px; /* Negative half of height. */
  margin-left: -50px; /* Negative half of width. */
  top: 50%;
  left: 50%;
  font-size: 50px;
  opacity: 0.3;
  transition: 0.3s;
  background: none;
  color: lightcyan;
  outline: none;
  border-radius: 1000px;
  cursor: pointer;
  cursor: pointer;
}

.myIcon:hover {
  opacity: 1;
  transition: 0.3;
  background: lightcyan;
  border-radius: 60px;
  color: black;
  box-shadow: 0px 0px 40px lightcyan;
}

.myIconclose {
  position: fixed;
  margin-top: -50px; /* Negative half of height. */
  margin-left: -50px; /* Negative half of width. */
  top: 50%;
  left: 50%;
  font-size: 50px;
  opacity: 0.3;
  transition: 0.3s;
  background: none;
  color: lightcyan;
  outline: none;
  border-radius: 1000px;
  cursor: pointer;
  cursor: pointer;
}

.myIconclose:hover {
  opacity: 1;
  transition: 0.3;
  background: red;
  border-radius: 60px;
  color: black;
  box-shadow: 0px 0px 60px red;
}

.git {
  transition: 0.8s;
  position: fixed;
  margin-top: -25px; /* Negative half of height. */
  margin-left: -25px; /* Negative half of width. */
  top: 40%;
  left: 35%;
  font-size: 25px;
  transition: 0.3s;
  background: none;
  color: lightcyan;
  outline: none;
  border-radius: 1000px;
  cursor: pointer;
  cursor: pointer;
}

.git:hover {
  opacity: 1;
  transition: 0.3;
  background: black;
  border-radius: 60px;
  color: coral;
  box-shadow: 0px 0px 60px coral;
}

.twitter {
  position: fixed;
  margin-top: -25px; /* Negative half of height. */
  margin-left: -25px; /* Negative half of width. */
  top: 30%;
  left: 50%;
  font-size: 25px;
  transition: 0.3s;
  background: none;
  color: lightcyan;
  outline: none;
  border-radius: 1000px;
  cursor: pointer;
  cursor: pointer;
}

.twitter:hover {
  opacity: 1;
  transition: 0.3;
  background: black;
  border-radius: 60px;
  color: cornflowerblue;
  box-shadow: 0px 0px 60px cornflowerblue;
}

.linkedin {
  position: fixed;
  margin-top: -25px; /* Negative half of height. */
  margin-left: -25px; /* Negative half of width. */
  top: 40%;
  left: 65%;
  font-size: 25px;
  transition: 0.3s;
  background: none;
  color: lightcyan;
  outline: none;
  border-radius: 1000px;
  cursor: pointer;
  cursor: pointer;
}

.linkedin:hover {
  opacity: 1;
  transition: 0.3;
  background: black;
  border-radius: 60px;
  color: greenyellow;
  box-shadow: 0px 0px 60px greenyellow;
}
</style>
