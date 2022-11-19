<template>
  <div id="page">
    <div>
      <video autoplay loop muted class="video">
        <source src="./assets/BeeBackground.mp4" type="video/webm">
        <source src="./assets/BeeBackground.mp4" type="video/mp4">
      </video>
      <h1 style="transform: translate(5.5%, 300%);">Welcome to SEARCH</h1>
    </div>
    
    <div>
      <div class="infoText" style="transform: translate(30vw, 95vh);">
        <h2 style="transform: translate(-25%, -27.5%);">What we do.</h2>
        <p class="bodyText" style="transform: translate(10%, -27.5%); width: 87.5%; text-align: left;">
          We are Purdue University's premiere space focused chapter. Our vision as a multidisciplinary
          organization of students, faculty, staff, and alumni is to add more members and partners to the Cradle of Astronauts as well as increase support for human spaceflight and space exploration.
        </p>
        <p class="bodyText" style="transform: translate(10%, -27.5%); width: 87.5%; text-align: left;">
          We were founded by passionate students of space and wish to grow through analog astronaut missions, outreach events with industry experts, national and global competitions, and skill building workshops. We wish to offer our members unique and hands-on learning experiences to constantly remind them why they fell in love with space.
        </p>
        <p class="bodyText" style="transform: translate(10%, -152.5%); width: 87.5%; text-align: left;">
          The organizational structure of SEARCH is split into three technical sub-teams:
        </p>
      </div>
      <img  id="mission" class="background" alt="Background" src="./assets/TreeBackground.png" style="transform: translate(-50%, 50%);">
    </div>

    <div>
      <div class="infoText" style="transform: translate(30vw, 127.5vh); height: 68vh;">
        <h2 style="transform: translate(3.5%, -12.5%); text-align: left;">The Mars Desert Research Station.</h2>
        <p class="bodyText" style="transform: translate(10%, -65%); width: 45vw; text-align: left;">
          The <a href="http://mdrs.marssociety.org/">MDRS</a> mission is to select an elite crew of students to represent Purdue for a two-week Mars-analog simulation in the desert of Utah. There, students perform innovative scientific experiments and simulate complete isolation to further advance the possibilities of Mars exploration.
        </p>
        <h3 style="transform: translate(3.5%, -160%); text-align: left;">Past Missions</h3>
        <div style="transform: translate(-10%, -185%)">
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
      <div style="transform: translate(0%, -5%)">
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
      </div>
      <img id="leadership" class="background" alt="Background" src="./assets/TreeBackground.png" style="transform: translate(-50%, 250%);">
    </div>

    <div>
      <div class="infoText" style="transform: translate(70%, 37.5%); height: 275px; width: 650px;">
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
  </div>


  <img class="logo" style="top: 70px; left: 145px;" alt="Vue logo" src="./assets/logo.png">
    <img class="logo" style="top: 70px; left: 10px;" alt="Vue logo" src="./assets/logo.png">
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
  }
}
</script>

<style>
#app {
  font-family: Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #000000; 
  margin: 0px;
}

html {
    max-width: 100%;
    overflow-x: hidden;
    margin: 0px;
}

.page {
  display: flex;
  flex-direction: row;
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
  font-size: 1.3vw;
  margin: 3vh;
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
  width: 54%;
  border: 1vw solid rgb(255, 255, 255);
  background-color: rgb(255, 255, 255);
  border-radius: 1.25vw;
  opacity: 0.75;
  margin: 0px;
}

h1 {
  font-size: 5.65vw;
}

h2 {
  font-size: 4.52vw;
}

h3 {
  font-size: 2.325vw;
}

h4 {
  font-size: 2.05vw;
}

.tab {
  display: inline-block;
  margin-left: 11.4vw;
}
</style>
