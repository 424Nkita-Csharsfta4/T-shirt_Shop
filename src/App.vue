<template>
 <div id="app">
  <Wrappermain/>
 </div>
</template>

<script>
import Wrappermain from './components/Wrappermain.vue'

export default {
  name: 'App',
  components: {
   Wrappermain
  }
}
</script>

<style>
#app{
  text-align: center;
  margin-top: 60px;
  font-family: 'Gill Sans', 'Gill Sans MT', Calibri, 'Trebuchet MS', sans-serif;
}
</style>
