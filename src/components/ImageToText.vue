<template>
<div>
    <h4 style="object-fit: cover; width: 13.2275132275vw; position: relative; transform: translate(0%, 125%);">{{name}}<br>{{title}}</h4>
    <div class="fade-in-image" style="position: absolute">
      <img :src="resolve_img_url(imageSrc)" />
    </div>
</div>
</template>

<script>

export default {
  name: 'ImageToText',
  props: {
    name: String,
    title: String,
    imageSrc: String
  },
  methods: {
    resolve_img_url: function (path) {
      let images = require.context('../assets/', false, /\.png$|\.jpg$/)
      return images("./"+path)
    }
  }
}
</script>

<style scoped>
.fade-in-image {
  opacity: 100%;
  transition: opacity 1s;
  max-width: 15%;
  margin: 0px;
}

.fade-in-image:hover {
  opacity: 0%;
  transition: opacity 1s;
  max-width: 15%;
  margin: 0px;
}

h4 {
  font-size: 2.05vw;
  margin: 0px;
  color: white;
}

img {
  width: 13.2275132275vw;
  height: 13.2275132275vw;
  margin: 0px;
  object-fit: cover;
}
</style>