<template>
  <div>
    <video :class="{'fade-out': !isIntersectingElement1}" autoplay loop muted class="video">
      <source src="./assets/BeeBackground.mp4" type="video/webm">
      <source src="./assets/BeeBackground.mp4" type="video/mp4">
    </video>
    <img class="logo" alt="Vue logo" src="./assets/logo.png">
    <img class="logo" alt="Vue logo" src="./assets/logo.png">
    <h1 style="transform: translate(8.5%, 75%);">Welcome to SEARCH</h1>
    <p>The intersection is here</p>
    <intersection-observer
        sentinal-name="sentinal-name"
        @on-intersection-element="onIntersectionElement1"
      ></intersection-observer>
  </div>
  
  <div id="secondSection">
    <p class="bodyText" style="transform: translate(75%, 800%); margin-bottom:50%">
      Look at me, I'm the main goal of the club in five to ten sentences.
      This is crazy, and no one has ever done this before. 
      Yes, this is indeed default text.
      But it would be funny if I just left this in the website.
      Maybe I'll leave an easter egg to unlock this.
      No, I won't. I'm a trustworthy, professional lad. 
      I'll probably even remove this before the leadership team meeting.
      If I don't, I'll get so much anxiety.
    </p>
    <p>The intersection is here</p>
    <intersection-observer
        sentinal-name="sentinal-name"
        @on-intersection-element="onIntersectionElement2"
      ></intersection-observer>
    <img class="background" :class="{'fade-out': !isIntersectingElement2}" alt="Background" src="./assets/TreeBackground.png" style="transform: translate(-50%, 50%);">
  </div>

  <div>
    <p>The intersection is here</p>
    <intersection-observer
        sentinal-name="sentinal-name"
        @on-intersection-element="onIntersectionElement3"
      ></intersection-observer>
    <img class="background" :class="{'fade-out': !isIntersectingElement3}" alt="Background" src="./assets/TreeBackground.png" style="transform: translate(-50%, 150%);">
  </div>

  <div>
    <p>The intersection is here</p>
    <intersection-observer
        sentinal-name="sentinal-name"
        @on-intersection-element="onIntersectionElement4"
      ></intersection-observer>
    <img class="background" :class="{'fade-out': !isIntersectingElement4}" alt="Background" src="./assets/TreeBackground.png" style="transform: translate(-50%, 250%);">
  </div>

  <div>
    <p>The intersection is here</p>
    <intersection-observer
        sentinal-name="sentinal-name"
        @on-intersection-element="onIntersectionElement5"
      ></intersection-observer>
    <img class="background" :class="{'fade-out': !isIntersectingElement5}" alt="Background" src="./assets/TreeBackground.png" style="transform: translate(-50%, 350%);">
  </div>

  <sidebar-menu :menu="menu" hideToggle="true" style="transform: translate(0%, 27.5%); height: 60%; border-radius: 25px;"/>
</template>

<script>
import IntersectionObserver from "./components/IntersectionObserver";
import { SidebarMenu } from 'vue-sidebar-menu'
import 'vue-sidebar-menu/dist/vue-sidebar-menu.css'

export default {
  name: 'App',
  components: {
    IntersectionObserver,
    SidebarMenu
  },
  data() {
    return {
      isIntersectingElement1: false,
      isIntersectingElement2: false,
      isIntersectingElement3: false,
      isIntersectingElement4: false,
      isIntersectingElement5: false,
      menu: [
          {
            header: 'Main Navigation',
            hiddenOnCollapse: true
          },
          {
            href: '#top',
            title: 'Dashboard',
            icon: 'fa fa-user'
          },
          {
            href: '#secondSection',
            title: 'Charts',
            icon: 'fa fa-chart-area',
            child: [
              {
                href: '/charts/sublink',
                title: 'Sub Link'
              }
            ]
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
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #ffffff; 
  margin-top: 60px;
}

.logo {
  margin: 20px;
  width: 7.5%;
  margin-top: -50px;
  transform: translate(-540%, 0%);
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

h1 {
  font-size: 80px;
}
</style>
