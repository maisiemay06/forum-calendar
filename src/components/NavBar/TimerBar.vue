<template>
  <!-- Countdown Bar -->

  <div class="w-full lg:px-20 border-box">
    <div
      class="
        w-full
        flex
        justify-around
        items-center
        bg-meeow-primary
        text-white
        rounded-b-lg
        py-2
        px-6
        top-[155px]
        lg:h-[80px] lg:top-[170px] lg:justify-center
        border-box
      "
    >
      <p class="hidden lg:inline-block font-semibold text-[15px] mr-5">
        on-demand networking in
      </p>
      <p class="text-3xl sm:text-[50px] font-semibold lg:mr-5">13:52</p>
      <button class="inline-block lg:hidden text-[15px] rounded-full">
        Open on-demand networking
      </button>

      <div
        @click="
          () => {
            openModal('ondemand');
            showOnDemandHelp = !showOnDemandHelp;
          }
        "
      >
        <img
          src="../../assets/imgs/info-bubble.png"
          alt=""
          class="hover:cursor-pointer inline"
        />
        <a class="hidden lg:inline-block text-xs ml-2 hover:cursor-pointer"
          >Tell me more about this?</a
        >

        <div
          class="
            bg-white
            drop-shadow-lg
            border
            rounded-tl-xl rounded-br-xl
            text-black text-left text-sm
            p-6
            w-[296px]
            absolute
            top-[250px]
            -ml-[3%]
            z-50
          "
          v-if="showOnDemandHelp"
          @click="showOnDemandHelp = false"
        >
          <p class>
            AI matched, On-demand networking on Meeow allows you to network with
            up to 3 new people on the hour, every hour for 45 mins.
            <br />
            Only 4 people in each meeting, to ensure good quality conversation.
            <br />
            No limit to the number of 4 person meetings at one time, so everyone
            gets to network when they want to.
          </p>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "TimerBar",
  props: ["openModal"],
  data() {
    return {
      showOnDemandHelp: false,
    };
  },
};
</script>