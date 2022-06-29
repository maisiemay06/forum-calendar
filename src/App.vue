<template>
  <nav-bar></nav-bar>
  <calendar-grid></calendar-grid>
</template>

<script>
import NavBar from "./components/NavBar/NavBar.vue";
import CalendarGrid from "./components/CalendarGrid.vue";

export default {
  name: "App",
  components: {
    NavBar,
    CalendarGrid,
  },
};
</script>

<style>
#app {
  font-family: "Sofia Pro", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
}
</style>
