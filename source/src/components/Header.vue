<template>
  <header>
    <h1>
      <vue-typer
        text="Hi I'm Ben"
        repeat="0"
        pre-type-delay="1500"
        type-delay="125"
        caret-animation="phase"
        :pre-erase-delay="30000"
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
  }),
}
</script>
<style lang="stylus">
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

  @media (max-width: 700px)
    min-height: 50vh

  .typed
    color: white

  h1
    color: white
    font-size: 4rem
    font-family: 'Source Code Pro'

    .vue-typer span.typed
      color: white

  a
    display: inline-block
    margin-top: 2.5rem
    padding: 0.6rem 1.75rem
    width: auto
    border: white 1px solid
    border-radius: 2rem
    color: white
    text-decoration: none

    &:not(:first-child)
      margin-left: 0.5rem

    &:hover
      background-color: alpha(white, 0.4)
</style>

