<template>
<div>
    <h4 style="object-fit: cover; width: 13.2275132275vw; position: relative; transform: translate(0%, 225%);">{{name}}</h4>
    <h4 style="object-fit: cover; width: 13.2275132275vw; position: relative; transform: translate(0%, 230%);">{{title}}</h4>
    <div class="fade-in-image" style="position: absolute">
      <img src="../assets/logo.png">
    </div>
</div>
</template>

<script>

export default {
  name: 'ImageToText',
  props: {
    name: String,
    title: String
  }
}
</script>

<style scoped>
.fade-in-image {
  opacity: 100%;
  transition: opacity 1s;
  background-color: rgb(255, 255, 255);
  max-width: 15%;
  margin: 0px;
}

.fade-in-image:hover {
  opacity: 0%;
  transition: opacity 1s;
  background-color: rgb(255, 255, 255);
  max-width: 15%;
  margin: 0px;
}

h4 {
  font-size: 2.05vw;
  margin: 0px;
}

img {
  width: 13.2275132275vw;
  margin: 0px;
}
</style>