<template>
  <nav-bar></nav-bar>
  <calendar-grid></calendar-grid>
  <mobile-calendar></mobile-calendar>
  <mobile-footer-nav></mobile-footer-nav>
</template>

<script>
import NavBar from "./components/NavBar/NavBar.vue";
import CalendarGrid from "./components/CalendarGrid.vue";
import MobileCalendar from "./components/MobileCalendar.vue";
import MobileFooterNav from "./components/NavBar/MobileFooterNav.vue";

export default {
  name: "App",
  components: {
    NavBar,
    CalendarGrid,
    MobileCalendar,
    MobileFooterNav,
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
