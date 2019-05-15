<template>
  <header>
    <h1>
      <vue-typer
        :text="text"
        :repeat="0"
        :pre-type-delay="1500"
        :type-delay="125"
        caret-animation="phase"
      />
    </h1>

    <a href="https://github.com/brownben">Check Out My Github</a>
  </header>
</template>
<script>
import { VueTyper } from 'vue-typer'

export default {
  components: {
    VueTyper,
  },

  data: () => ({
    dark: false,
    countWord: 0,
    text: 'Hi I\'m Ben',
  }),

  mounted: function () {
    window.addEventListener('resize', this.handleResize)
    this.handleResize()
  },

  destroyed () {
    window.removeEventListener('resize', this.handleResize)
  },

  methods: {
    handleResize: function () {
      if (window.innerWidth <= 700) this.text = 'Hi I\'m\nBen'
      else this.text = 'Hi I\'m Ben'
    },
  },
}
</script>
<style lang="stylus">
@font-face
  font-weight: 400
  font-style: normal
  font-family: 'Source Code Pro'
  src: local('Source Code Pro'), local('SourceCodePro-Regular'), url('https://fonts.gstatic.com/l/font?kit=HI_SiYsKILxRpg3hIP6sJ7fM7PqVP_nbk4Vnjw3VYWo&skey=d94d317bc78fd84e&v=v9') format('woff2')
  font-display: fallback

header
  display: flex
  flex-direction: column
  justify-content: center
  align-items: center
  margin-bottom: 1.5rem
  padding: 3rem 1rem
  min-height: 40vh
  background: linear-gradient(#0D47A1, #1976D2)
  box-shadow: 0 4px 5px 0 rgba(0, 0, 0, 0.14), 0 1px 10px 0 rgba(0, 0, 0, 0.12), 0 2px 4px -1px rgba(0, 0, 0, 0.3)
  text-align: center
  transition: 0.5s

  @media (max-width: 700px)
    min-height: 50vh

    h1
      font-size: 3.5rem

  .typed
    color: white

  h1
    min-height: 5rem
    color: white
    font-size: 4rem
    font-family: 'Source Code Pro', Inconsolata, 'Courier New', Courier, monospace

    .vue-typer span.typed
      color: white

  a
    display: inline-block
    margin-top: 3rem
    padding: 0.6rem 1.75rem
    width: auto
    outline: 0
    border: white 1px solid
    border-radius: 2rem
    color: white
    text-decoration: none

    &:not(:first-child)
      margin-left: 0.5rem

    &:hover
      background-color: alpha(white, 0.4)

span.nowrap
  white-space: nowrap
  word-wrap: break-word
</style>

