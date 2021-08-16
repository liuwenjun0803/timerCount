<template>
  <div id="app">
    <Head/>

  </div>
</template>

<script>
import Head from './components/Head.vue'
import Foot from './components/Foot.vue'
import MajorClock from './components/MajorClock.vue'
import ControlButton from './components/ControlButton.vue'
import SplitTimes from './components/SplitTimes.vue'
export default {
  name: 'App',
  components: {
    Head,
    Foot,
    MajorClock,
    ControlButton,
    SplitTimes
  }
}
</script>

<style lang="scss">
*{
  margin: 0;
  padding: 0;
  box-sizing: border-box;
  list-style: none;
}
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
