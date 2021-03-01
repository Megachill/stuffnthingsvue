<template>
  <div id="app">
    <post-index></post-index>
  </div>
</template>

<script>
import PostIndex from "@/components/PostIndex"

export default {
  name: 'App',
  components: {
    PostIndex,
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
