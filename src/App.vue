<template>
  <div id="app">
    <TimezoneClock />
  </div>
</template>

<script>
import TimezoneClock from "./components/TimezoneClock";

export default {
  name: "App",
  components: {
    TimezoneClock
  }
};
</script>

<style>
#app {
  text-align: center;
}
</style>
