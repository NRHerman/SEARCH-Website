<template>
  <div>
    <video autoplay loop muted class="video">
      <source src="./assets/BeeBackground.mp4" type="video/webm">
      <source src="./assets/BeeBackground.mp4" type="video/mp4">
    </video>
    <img class="logo" style="top: 70px; left: 145px;" alt="Vue logo" src="./assets/logo.png">
    <img class="logo" style="top: 70px; left: 10px;" alt="Vue logo" src="./assets/logo.png">
    <h1 style="transform: translate(5.5%, 300%);">Welcome to SEARCH</h1>
  </div>
  
  <div>
    <div class="infoText" style="transform: translate(50%, 230%);">
      <h2 style="transform: translate(-25%, -27.5%);">What we do.</h2>
      <p class="bodyText" style="transform: translate(10%, -22.5%); width: 700px; text-align: left;">
        Look at me, I'm the main goal of the club in five to ten sentences.
        This is crazy, and no one has ever done this before. 
        Yes, this is indeed default text.
        But it would be funny if I just left this in the website.
        Maybe I'll leave an easter egg to unlock this.
        No, I won't. I'm a trustworthy, professional lad. 
        I'll probably even remove this before the leadership team meeting.
        If I don't, I'll get so much anxiety.
        Look at me, I'm the main goal of the club repeated in five to ten sentences.
        This is crazy, and no one has ever done this before.
      </p>
    </div>
    <img  id="mission" class="background" alt="Background" src="./assets/TreeBackground.png" style="transform: translate(-50%, 50%);">
  </div>

  <div>
    <div class="infoText" style="transform: translate(50%, 195%); height: 600px;">
      <h2 style="transform: translate(3.5%, -12.5%); text-align: left;">The Mars Desert Research Station.</h2>
      <p class="bodyText" style="transform: translate(10%, -65%); width: 700px; text-align: left;">
        Look at <a href="http://mdrs.marssociety.org/">me</a>, I'm the main goal of the club in five to ten sentences.
        This is crazy, and no one has ever done this before. 
        Yes, this is indeed default text.
      </p>
      <h3 style="transform: translate(3.5%, -55%); text-align: left;">Past Missions</h3>
      <div style="transform: translate(-10%, 0%)">
        <a href="http://mdrs.marssociety.org/">
         <img class="button" alt="logo" src="./assets/logo.png" style="transform: translate(-200%, 20%)">
        </a>
        <a href="http://mdrs.marssociety.org/">
         <img class="button" alt="logo" src="./assets/logo.png" style="transform: translate(0%, 20%)">
        </a>
        <a href="http://mdrs.marssociety.org/">
         <img class="button" alt="logo" src="./assets/logo.png" style="transform: translate(200%, 20%)">
        </a>
        <h4 style="transform: translate(10%, 330%)">2018<span class="tab"></span>2019<span class="tab"></span>2020</h4>
      </div>
    </div>
    <img id="MDRS" class="background" alt="Background" src="./assets/TreeBackground.png" style="transform: translate(-50%, 150%);">
  </div>

  <div>
    <image-to-text name="Really Long Name" title="Equally Long Title" style="transform: translate(20%, 710%)"></image-to-text>
    <image-to-text name="Really Long Name" title="Equally Long Title" style="transform: translate(35%, 587.5%)"></image-to-text>
    <image-to-text name="Really Long Name" title="Equally Long Title" style="transform: translate(50%, 465%)"></image-to-text>
    <image-to-text name="Really Long Name" title="Equally Long Title" style="transform: translate(65%, 342.5%)"></image-to-text>
    <image-to-text name="Really Long Name" title="Equally Long Title" style="transform: translate(80%, 220%)"></image-to-text>
    <image-to-text name="Really Long Name" title="Equally Long Title" style="transform: translate(20%, 247.5%)"></image-to-text>
    <image-to-text name="Really Long Name" title="Equally Long Title" style="transform: translate(35%, 125%)"></image-to-text>
    <image-to-text name="Really Long Name" title="Equally Long Title" style="transform: translate(50%, 2.5%)"></image-to-text>
    <image-to-text name="Really Long Name" title="Equally Long Title" style="transform: translate(65%, -120%)"></image-to-text>
    <image-to-text name="Really Long Name" title="Equally Long Title" style="transform: translate(80%, -242.5%)"></image-to-text>
    <img id="leadership" class="background" alt="Background" src="./assets/TreeBackground.png" style="transform: translate(-50%, 250%);">
  </div>

  <div>
    <div class="infoText" style="transform: translate(75%, 80%); height: 275px; width: 650px;">
      <h2 style="transform: translate(0%, 0%)">Contact Us</h2>

      <a href="http://mdrs.marssociety.org/">
        <img class="button" alt="logo" src="./assets/logo.png" style="transform: translate(-175%, 30%);">
      </a>
      <a href="http://mdrs.marssociety.org/">
        <img class="button" alt="logo" src="./assets/logo.png" style="transform: translate(45%, 30%);">
      </a>
    </div>

    <img id="joinUs" class="background" alt="Background" src="./assets/TreeBackground.png" style="transform: translate(-50%, 350%);">
  </div>

  <sidebar-menu :menu="menu" hideToggle="true" style="transform: translate(30%, 100%); height: 30%; width: 12.5%; border-radius: 25px; background-color: transparent;"/>
</template>

<script>
import { SidebarMenu } from 'vue-sidebar-menu'
import 'vue-sidebar-menu/dist/vue-sidebar-menu.css'
import ImageToText from "./components/ImageToText"

export default {
  name: 'App',
  components: {
    SidebarMenu,
    ImageToText
  },
  data() {
    return {
      menu: [
          {
            hiddenOnCollapse: true,
            header: 'SEARCH',
          },
          {
            href: '#mission',
            title: 'Mission',
            icon: 'fa fa-user'
          },
          {
            href: '#MDRS',
            title: 'MDRS',
            icon: 'fa fa-user',
          },
          {
            href: '#leadership',
            title: 'Leadership',
            icon: 'fa fa-user',
          },
          {
            href: '#joinUs',
            title: 'Join Us',
            icon: 'fa fa-user',
          }
        ]
    }
  },
  methods: {
    onIntersectionElement1(value) {
      this.isIntersectingElement1 = value;
    },
    onIntersectionElement2(value) {
      this.isIntersectingElement2 = value;
    },
    onIntersectionElement3(value) {
      this.isIntersectingElement3 = value;
    },
    onIntersectionElement4(value) {
      this.isIntersectingElement4 = value;
    },
    onIntersectionElement5(value) {
      this.isIntersectingElement5 = value;
    },
  },
}
</script>

<style>
#app {
  font-family: Helvetica, Avenir, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #000000; 
  margin-top: 60px;
}

html {
    max-width: 100%;
    overflow-x: hidden;
}

.logo {
  margin: 20px;
  width: 7.5%;
  margin-top: -50px;
  position: fixed;
}

.button {
  margin: 20px;
  width: 15%;
  margin-top: -50px;
  position: fixed;
}

.background {
  z-index: -1000;
  left: 50%;
  width: 100vw;
  height: 100vh;
  position: absolute;
  top: 50%;
  -webkit-transform: translate(-50%, -50%);
  -moz-transform: translate(-50%, -50%);
  -ms-transform: translate(-50%, -50%);
  transform: translate(-50%, 50%);
  object-fit: cover;
  transition: opacity 0.3s;
}

.background.fade-out {
  opacity: 0;
}

.bodyText {
  width: 50%;
  transform: translate(75%, 800%);
  font-size: 20px;
}

video {
  z-index: -1000;
  left: 50%;
  width: 100vw;
  height: 100vh;
  position: absolute;
  top: 50%;
  -webkit-transform: translate(-50%, -50%);
  -moz-transform: translate(-50%, -50%);
  -ms-transform: translate(-50%, -50%);
  transform: translate(-50%, -50%);
  object-fit: cover;
  transition: opacity 0.3s;
}

.video.fade-out {
  opacity: 0;
}

.infoText {
  height: 340px;
  width: 800px;
  border: 20px solid rgb(255, 255, 255);
  background-color: rgb(255, 255, 255);
  border-radius: 25px;
  opacity: 0.75;
}

h1 {
  font-size: 80px;
}

h2 {
  font-size: 60px;
}

h3 {
  font-size: 40px;
}

h4 {
  font-size: 30px;
}

.tab {
  display: inline-block;
  margin-left: 173.5px;
}
</style>
