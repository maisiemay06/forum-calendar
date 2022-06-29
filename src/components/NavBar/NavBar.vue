<template>
  <nav class="z-40 navbar">
    <main-nav :openModal="openModal"></main-nav>
    <search-bar></search-bar>
    <timer-bar :openModal="openModal"></timer-bar>
    <mobile-date-picker></mobile-date-picker>
    <modal-template
      v-if="showModal"
      class="z-30"
      :closeModal="closeModal"
      :modalContent="modalContent"
      :modalBtnContent="modalBtnContent"
    ></modal-template>
  </nav>
</template>

<script>
import ModalTemplate from "../ModalTemplate.vue";

import MainNav from "./MainNav.vue";
import SearchBar from "./SearchBar.vue";
import TimerBar from "./TimerBar.vue";
import MobileDatePicker from "./MobileDatePicker.vue";

export default {
  name: "NavBar",
  components: {
    ModalTemplate,
    MainNav,
    SearchBar,
    TimerBar,
    MobileDatePicker,
  },
  data() {
    return {
      showNavMenu: false,
      showModal: false,
      modalContent: "",
      modalBtnContent: "",
      showNavbar: true,
      lastScrollPos: 0,
    };
  },
  methods: {
    toggleNavMenu() {
      this.showNavMenu = !this.showNavMenu;
    },
    openModal(props) {
      if (props === "points") {
        this.modalContent = `Meeow awards every member points for every engagement with the community, helping you to build your reputation as a brilliant networker.
        As you build your points total and rise through the ranks tobe an
        Ambassador`;
        this.modalBtnContent = "Join now";
      } else if (props === "ondemand") {
        this.modalContent = `AI matched, On-demand networking on Meeow allows you to network with up to 3 new people on the hour, every hour for 45 mins.
        Only 4 people in each meeting, to ensure good quality conversation.
        No limit to the number of 4 person meetings at one time, so everyone gets to network when they want to.
        `;
        this.modalBtnContent = "Open on-demand networking";
      }
      this.showModal = true;
    },
    closeModal() {
      this.showModal = false;
    },
  },
};
</script>

<style scoped>
</style>