<template>
  <div>
    <h1>My Projects</h1>
    <div id="projects">
      <div id="nevis" class="project">
        <img src="@/assets/Nevis Logo.png" alt="Nevis Logo">
        <h2>Nevis</h2>
        <p>Event management software for orienteering is designed to be quick and easy to use. It can read SI Cards over a serial connection and has live views of Entries + Results. Created using Electron and Vue</p>
        <a href="https://brownben.github.io/nevis">Visit Website</a>
      </div>
      <div id="munro" class="project">
        <img src="@/assets/Munro Logo.png" alt="Munro Logo">
        <h2>Munro</h2>
        <p>
          My Advanced Higher Computing Project, a dynamic SPA which calculates the results for a league of orienteering events and allows sorting and filtering of results. Interacts with a backend API made with
          Flask
        </p>
        <a href="https://munro-leagues.herokuapp.com">View Website</a>
      </div>
      <div id="simon" class="project">
        <img src="@/assets/SimonGrid.png" alt="Simon Game Grid">
        <h2>Simon</h2>
        <p>A simple memory game based on the popular Simon Game built using Vanilla JS, HTML5, Stylus and the Web Audio API</p>
        <span>
          <a href="https://github.com/brownben/simon-game">View Source</a>
          <a href="https://brownben.github.io/simon-game">View Demo</a>
        </span>
      </div>
      <div id="maze-checker" class="project">
        <img src="@/assets/WOD Color.png" alt="World Orienteering Day Logo">
        <h2>Maze Checker</h2>
        <p>Checks if a simple maze orienteering course is completed correctly, by reading SI Cards and operates a simple leaderboard. Created using Electron for World Orienteering Day 2018</p>
        <a href="https://brownben.github.io/maze-checker">Visit Website</a>
      </div>
      <div id="circuit-timer" class="project">
        <img v-if="!dark" src="@/assets/Timer.png" alt="Clock - 00:00">
        <img v-else src="@/assets/TimerInverse.png" alt="Clock - 00:00">
        <h2>Circuit Timer</h2>
        <p>A timer for circuit training which beeps and displays a countdown for how much longer there is left in the current activity. Built using Promises and the Web Audio API with Vanilla JS, HTML and Stylus.</p>
        <a href="https://brownben.github.io/nevis">Visit Website</a>
      </div>
    </div>
  </div>
</template>
<script>
export default {
  props: {
    dark: {
      type: Boolean,
      default: false,
    },
  },
}
</script>

<style lang="stylus" scoped>
#projects
  display: grid
  margin-top: 1.5rem
  text-align: center
  font-weight: 300
  grid-template-columns: 1fr 1fr
  grid-gap: 1.5rem

  @media (max-width: 700px)
    grid-template-columns: 1fr

  .project
    display: flex
    flex-direction: column
    justify-content: space-evenly
    align-items: center
    padding: 1rem
    border: 1px solid #f0f0f0
    background-color: #fcfcfc

  h2
    font-size: 1.65rem

  img, h2, p, a
    margin-top: 0.25rem
    margin-bottom: 0.25rem

  img
    max-width: 38vw
    max-height: 150px

    @media (max-width: 700px)
      max-width: 80vw

  a
    display: inline-block
    margin-top: 0.5rem
    padding: 0.35rem 1rem
    width: auto
    border: #e0e0e0 1px solid
    color: black
    text-decoration: none

    &:not(:first-child)
      margin-left: 0.5rem

    &:hover
      background-color: #f0f0f0
</style>
