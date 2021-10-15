<template>
  <div id="app">
    <section :style="landing">
      <div class="header">
        <div class="navigation">
          <a-row>
            <a-col :xs="2" :sm="4" :md="6" :lg="4" :xl="10"></a-col>
            <a-col :xs="2" :sm="4" :md="6" :lg="20" :xl="10" class="navbar">
              <a-menu v-model="current" mode="horizontal">
                <a-menu-item key="home">
                  <a-icon type="home" />Home
                </a-menu-item>
                <a-menu-item key="settings">
                  <a-icon type="HeartOutlined" />About us</a-menu-item
                >
                <a-menu-item key="facebook">
                  <a-icon type="facebook" />Feautures
                </a-menu-item>
                <a-menu-item key="mail">
                  <a-icon type="mail" />Get started
                </a-menu-item>

                <a-menu-item key="log">
                  <a-button>Login</a-button>
                  <a-button>Sign Up</a-button>
                </a-menu-item>
              </a-menu>
            </a-col>
          </a-row>
        </div>
      </div>
      <div class="panel">
          <div class="left-panel">
               <h2 :style="headerTitleStyles">The os operation for Businesses</h2>
          <p :style="headerParaStyles">
            Lorem Ipsum has been the industry's standard dummy text ever since
            the 1500s, when an unknown printer took a galley of type and
            scrambled it to make a type specimen book. It has survived not only
            five centuries, but also the leap into electronic typesetting,
            remaining essentially unchanged.
          </p>
          <a-button :style="getStartedBtnStyles">Get-started</a-button>
          </div>
          <div class="right-panel">
               <img :src="require('../static/top-vctr.png')" class="top-img" />
          <img
            :src="require('../static/undraw_Mobile_marketing_re_p77p 1.png')"
          />
          </div>
      </div>
    </section>
    <section>
      <hr :style="hrStyles" />
    </section>
    <section>
        <div class="features">
            <Features/>
        </div>
    </section>

    <section>
        <div class="clients">
            <Clients/>
        </div>
    </section>
  </div>
</template>
<script>
import Header from "./header.vue";
import Features from "./features.vue"
import Clients from "./clients.vue"

export default {
  name: "Home",
  components: {
    Header,
    Features,
    Clients
  },
  data() {
    return {
      navigationStyles: {
        "font-size": "12px",
        "background": "transparent",
        // "z-index":"999"
      },
      headerStyles: {
        "font-weight": "light",
      },
      headerTitleStyles: {
        "margin-top": "10em",
        "margin-left": "4em",
        "font-size": "15px",
        "font-weight": "bold",
      },
      headerParaStyles: {
        "margin-top": "2em",
        "margin-left": "5em",
        "font-size": "12px",
      },
      getStartedBtnStyles: {
        "margin-top": "2em",
        "margin-left": "5em",
        "font-size": "12px",
        "background-color": "#FFD335",
      },
      hrStyles: {
        width: "30em",
        padding: "0.02em",
        "background-color": "#FFD335",
      },
    };
  },
};
</script>
<style scoped>
@import url("https://fonts.googleapis.com/css2?family=Poppins:wght@100;300&display=swap");

#app {
  background-color: #ffffff;
  font-family: Poppins;
}
.panel{
    display: flex;
}
.left-panel{
    width: 50%;
}
.navbar{
  z-index: 2;
  background: transparent;
}
a-menu{
    background: transparent;
}
img:nth-child(2) {
  width: 30em;
}
.right-panel .top-img {
  position: absolute;
  top: 0;
  right: 0;
  margin:0;
  width: 30em;
  /* z-index: -999; */
}
.features{
    margin-left:8em;
}
.clients{
    margin-top: 4em;
    margin-left: 3em;
}
</style>