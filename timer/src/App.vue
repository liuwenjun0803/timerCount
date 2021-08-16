<template>
  <div id="app">
    <Head/>
    <MajorClock/>
    <ControlButtons/>
    <SplitTimes/>
    <Foot/>
  </div>
</template>

<script>
import Head from './components/Head.vue'
import Foot from './components/Foot.vue'
import MajorClock from './components/MajorClock.vue'
import ControlButtons from './components/ControlButtons.vue'
import SplitTimes from './components/SplitTimes.vue'
export default {
  name: 'App',
  components: {
    Head,
    Foot,
    MajorClock,
    ControlButtons,
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
a{
  text-decoration: none;
  color: #7e7e7e;
}
html{
  font-size: 16px;
  background: rgb(10, 10, 10);
}
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  text-align: center;
  width: 100vw;
  height: 100vh;
  display: flex;
  flex-direction: column;
}
</style>
