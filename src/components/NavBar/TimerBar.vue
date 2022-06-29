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

      <img
        src="../../assets/imgs/info-bubble.png"
        alt=""
        class="hover:cursor-pointer"
        @click="() => openModal('ondemand')"
      />
      <a
        class="hidden lg:inline-block text-xs ml-2 hover:cursor-pointer"
        @click="() => openModal('ondemand')"
        >Tell me more about this?</a
      >
    </div>
  </div>
</template>

<script>
export default {
  name: "TimerBar",
  props: ["openModal"],
};
</script>