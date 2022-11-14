<template>
<div>
    <h4 style="object-fit: cover; width: 200px; position: relative; transform: translate(0%, 325%);">{{name}}</h4>
    <h4 style="object-fit: cover;  width: 200px; position: relative; transform: translate(0%, 325%);">{{title}}</h4>
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
}

.fade-in-image:hover {
  opacity: 0%;
  transition: opacity 1s;
  background-color: rgb(255, 255, 255);
  max-width: 15%;
}

h4 {
  font-size: 30px;
}
</style>