<template>
  <div>
    <h1>Page Not Found</h1>
    <p>Sorry The Page You Were Looking For Could Not Be Found</p>
    <div>
      <a @click="$router.push('/')">Return Home</a>
      <a @click="$router.go(-1)">Go Back</a>
    </div>
  </div>
</template>
<style lang="stylus" scoped>
p
  padding: 1rem 0
  font-size: 1.15rem

a
  display: inline-block
  margin: 0
  padding: 0.5rem 1.25rem
  width: auto
  border: #e0e0e0 1px solid
  background-color: white
  color: black
  text-decoration: none
  font-size: 1rem

  &:hover
    background-color: #f0f0f0

  &:not(:first-child)
    margin-left: 0.5rem
</style>

