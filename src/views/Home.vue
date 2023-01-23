<template>
  <div class="home">
    <div id="read"></div>
  </div>
</template>

<script>
import Epub from 'epubjs'

global.Epub = Epub
export default {
  name: 'home',
  mounted() {
    this.book = new Epub('/test.epub')
    console.log(this.book)
    this.book.renderTo('read', {
      width: window.innerWidth,
      height: window.innerHeight
    }).display()
  }
}
</script>