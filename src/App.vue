<template>
  <div>
    <p>The intersection is here</p>
    <intersection-observer
        sentinal-name="sentinal-name"
        @on-intersection-element="onIntersectionElement1"
      ></intersection-observer>
    <video :class="{'fade-out': !isIntersectingElement1}" autoplay loop muted class="video">
      <source src="./assets/BeeBackground.mp4" type="video/webm">
      <source src="./assets/BeeBackground.mp4" type="video/mp4">
    </video>
    <img class="logo" alt="Vue logo" src="./assets/logo.png">
    <img class="logo" alt="Vue logo" src="./assets/logo.png">
  </div>
  
  <div>
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
</template>

<script>
import IntersectionObserver from "./components/IntersectionObserver";

export default {
  name: 'App',
  components: {
    IntersectionObserver
  },
  data() {
    return {
      isIntersectingElement1: false,
      isIntersectingElement2: false,
      isIntersectingElement3: false,
      isIntersectingElement4: false,
      isIntersectingElement5: false,
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
  color: #2c3e50;
  margin-top: 60px;
}

.logo {
  margin: 120px;
  width: 7.5%;
  margin-top: -50px;
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
</style>
