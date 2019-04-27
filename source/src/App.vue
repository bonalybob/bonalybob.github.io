<template>
  <div id="app" :class="{dark: dark}">
    <page-header />
    <main>
      <router-view :dark="dark" />
    </main>
    <footer>
      <button v-if="dark" @click="dark = false">Use Light Theme</button>
      <button v-else @click="dark = true">Use Dark Theme</button>
      <p>Created by Ben Brown 2019</p>
    </footer>
  </div>
</template>

<script>
import Header from '@/components/Header'

export default {
  components: {
    'page-header': Header,
  },
  data: () => ({
    dark: false,
  }),
}
</script>
<style lang="stylus">
@import url('https://fonts.googleapis.com/css?family=Source+Code+Pro')

#app
  min-height: 100vh

html, body
  width: 100%

html, body, p, a, h1, h2, h3, h4, h5, h6, b, button, div, img
  margin: 0
  padding: 0
  font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen, Ubuntu, Cantarell, 'Open Sans', 'Helvetica Neue', sans-serif
  transition: 0.3s

main
  box-sizing: border-box
  padding: 0 5vw
  width: 100%

footer
  text-align: center

  button
    display: inline-block
    margin: 1.5rem 0 0.5rem
    padding: 0.6rem 1.75rem
    width: auto
    outline: 0
    border: #e0e0e0 1px solid
    border-radius: 2rem
    background-color: white
    color: black
    text-decoration: none
    font-size: 1rem

    &:not(:first-child)
      margin-left: 0.5rem

    &:hover
      background-color: #f0f0f0

  p
    padding: 1rem
    font-size: 1.15rem

.vue-typer .custom.caret
  width: 4px
  background-color: white

  &.complete
    display: inline-block

.dark
  background: black !important
  background-color: black !important
  color: white !important

  header
    background: black !important
    background-color: black !important
    box-shadow: none !important

    .typed
      color: white !important

  a, button
    border: white 1px solid !important
    background-color: alpha(white, 0) !important
    color: white !important

    &:hover
      background-color: alpha(white, 0.4) !important

  #projects
    .project
      background-color: black !important
      color: white !important

      a
        color: white !important
</style>

