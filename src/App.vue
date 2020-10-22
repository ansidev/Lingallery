<template>
  <div id="app">
    <lingallery
      :addons="{ enableLargeView: true, enablePictureElement: true }"
      :square-mode-desktop="true"
      :responsive="true"
      :items="[
        {
          src: 'https://picsum.photos/600/600/?image=0',
          alt: 'Some alt text',
          thumbnail: 'https://picsum.photos/64/64/?image=0',
          caption: 'Some Caption',
          largeViewSrc: 'https://picsum.photos/2000/2000/?image=0',
          pictureElement: [
            {
              srcset: 'https://picsum.photos/1200/1200/?image=0',
              media: '(min-width: 600px)',
              type: 'image/jpg'
            },
            {
              srcset: 'https://picsum.photos/1200/1201/?image=0',
              media: '(min-width: 600px)',
              type: 'image/webp'
            },
            {
              srcset: 'https://picsum.photos/2000/2000/?image=0',
              media: '(min-width: 1200px)'
            }
          ]
        }
      ]"
    />
  </div>
</template>

<script>
import Lingallery from './components/Lingallery.vue'

export default {
  name: 'App',
  components: {
    Lingallery
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
