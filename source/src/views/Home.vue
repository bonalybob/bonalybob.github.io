<template>
  <div>
    <h1 class="title">My Projects</h1>
    <div class="projects">
      <div class="project munro">
        <div class="screenshot" aria-label="Screenshot of Munro on Desktop and Mobile" />
        <div class="info">
          <h1>Munro</h1>
          <p>Originally created as part of my Advanced Higher Computing project, Munro is a Single Page VueJS App with a RESTful style Python Flask API. Munro calculates and displays the results for a league of Orienteering events, with options to search and sort the results. It also allows the league administrator to login and update all the details for the league and upload the results file for processing. Designed and created based off Orienteers feedback from what they wanted from the system.</p>
          <div class="links">
            <a href="https://munro-leagues.herokuapp.com">Visit Website</a>
          </div>
        </div>
      </div>
      <div class="project nevis">
        <div class="screenshot" aria-label="Screenshot of Nevis" />
        <div class="info">
          <h1>Nevis</h1>
          <p>Simple, Easy to Use Event Management Software for Orienteering created using Electron and VueJS. It is designed to allow as many people as possible to run the timing systems at Orienteering events. Read the raw data from the timing chips through the serial port and then calculates the times and results based off the data imported and the entries and course data entered. Results can then be exported in a range of formats. Includes advanced course matching, live search and sort of entries and support for the SI Card archive coming soon.</p>
          <div class="links">
            <a href="https://brownben.github.io/nevis">Visit Website</a>
            <a href="https://github.com/brownben/nevis">View Source</a>
          </div>
        </div>
      </div>
      <div class="project small simon">
        <div class="screenshot" aria-label="Screenshot of Simon Game" />
        <div class="info">
          <h1>Simon Game</h1>
          <p>A simple memory game based on the popular Simon Game. Built using Vanilla JS, HTML5, Stylus and the Web Audio API.</p>
          <div class="links">
            <a href="https://github.com/brownben/simon-game">View Source</a>
            <a href="https://brownben.github.io/simon-game">View Demo</a>
          </div>
        </div>
      </div>
      <div class="project small circuits">
        <div class="screenshot" aria-label="Screenshot of Circuit Timer" />
        <div class="info">
          <h1>Circuits Timer</h1>
          <p>A Progressive Web App which acts as a timer for Circuit Training activities, displaying a countdown clock and beeping using the Web Audio API. It has support for offline use, to allow users to train without a mobile signal. Created using Vanilla JS, Stylus and HTML5</p>
          <div class="links">
            <a href="https://github.com/brownben/simon-game">View Source</a>
            <a href="https://brownben.github.io/simon-game">View Demo</a>
          </div>
        </div>
      </div>
      <div class="project small wodmaze">
        <div class="screenshot" aria-label="Screenshot of World Orieenteering Day Maze Checker" />
        <div class="info">
          <h1>WOD Maze Checker</h1>
          <p>Originally created for World Orienteering Day in 2018, it is designed to read the timing chips and check a simple maze orienteering course is completed correctly, keeping a simple scoreboard with the winners time. Serial proccessing logic based off of a simplified version of Nevis to make even easier to use. Created using Electron</p>
          <div class="links">
            <a href="https://brownben.github.io/maze-checker">Visit Website</a>
          </div>
        </div>
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
.title
  padding: 1rem 0
  font-size: 2.5rem

.munro .screenshot
  background-image: url('../assets/MunroScreenshot.png')

.nevis .screenshot
  background-image: url('../assets/NevisScreenshot.png')

.simon .screenshot
  background-image: url('../assets/SimonScreenshot.png')

.wodmaze .screenshot
  background-image: url('../assets/WODMazeScreenshot.png')

.circuits .screenshot
  background-image: url('../assets/CircuitsScreenshot.png')

.project
  display: flex
  flex-direction: row
  justify-content: space-evenly
  align-content: center
  padding: 3rem 0

  .screenshot
    box-sizing: border-box
    min-height: 200px
    width: 50%
    background-position: center
    background-size: contain
    background-repeat: no-repeat

  &.small
    display: inline-flex
    flex-direction: column
    box-sizing: border-box
    padding: 1rem 0.5rem
    width: 50%
    text-align: center

    .info
      margin: 0
      padding: 0
      width: 100%

    .screenshot
      margin: 0.5rem
      min-height: 200px
      width: 100%

    @media (max-width: 800px)
      width: 100%

  .info
    display: inline-flex
    flex-direction: column
    justify-content: center
    box-sizing: border-box
    margin-left: 2rem
    width: calc(50% - 2rem)

    @media (max-width: 1000px)
      margin: 0
      padding: 0

    h1
      padding: 0.5rem 0
      font-size: 2.75rem

    p
      padding: 0.35rem 0
      font-size: 1rem

    a
      display: inline-block
      margin: 0.75rem 0
      padding: 0.45rem 0.8rem
      width: auto
      border: #e0e0e0 1px solid
      color: black
      text-decoration: none

      &:not(:first-child)
        margin-left: 0.5rem

      &:hover
        background-color: #f0f0f0

  @media (max-width: 1000px)
    display: block
    padding: 1.5rem 0
    text-align: center

    .screenshot
      display: block
      padding: 1rem 10%
      width: 100%

    .info
      display: block
      width: 100%
      text-align: center

  @media (max-width: 700px)
    .screenshot
      padding: 1rem 5%
</style>
