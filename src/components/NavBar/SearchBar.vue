<template>
  <!-- Search Bar -->
  <div
    class="
      w-full
      flex
      justify-between
      items-center
      bg-white
      top-[100px]
      lg:top-[90px]
      h-[55px]
      lg:px-20 lg:py-3 lg:h-[80px] lg:drop-shadow-md
    "
  >
    <!-- Desktop Date Picker -->
    <a href=""
      ><i class="hidden lg:inline-block fa-solid fa-chevron-left mr-5"></i
    ></a>
    <p class="hidden lg:inline-block text-[15px] mr-5">January 2022</p>
    <a href=""
      ><i class="hidden lg:inline-block fa-solid fa-chevron-right mr-5"></i
    ></a>
    <button
      class="
        hidden
        lg:inline-block
        border border-black
        px-5
        h-7
        rounded-full
        mr-5
        text-sm
        hover:border-2
        box-border
      "
    >
      Today
    </button>

    <!-- Desktop Book Buddies Help Btn & Modal -->
    <div>
      <button
        class="
          hidden
          lg:inline-block
          bg-[#FAFAFA]
          px-5
          h-7
          rounded-tl-lg rounded-br-lg
          mr-5
          text-sm
          hover:bg-[#F4F4F4]
        "
        @click="
          showIndicatorHelp = !showIndicatorHelp;
          showColourCodeHelp = false;
        "
      >
        <img
          src="../../assets/imgs/buddie-blue.png"
          alt="blue book buddie"
          class="inline mr-1"
        />
        What do these mean?
      </button>

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
          top-[80%]
          -ml-[3%]
          z-50
        "
        v-if="showIndicatorHelp"
        @click="showIndicatorHelp = false"
      >
        <p class="mb-3">
          Booking indicators tell you how many members have already booked to
          network in that hour.
          <br />
          There’s no limit to number of members that can network every hour.
          Meeow will match you into rooms of up to 4.
        </p>
        <div>
          <img
            src="../../assets/imgs/buddie-clear.png"
            alt=""
            class="inline mr-3 mb-3 w-4"
          />
          <p class="inline">1 > 2 members have booked</p>
        </div>
        <div>
          <img
            src="../../assets/imgs/buddie-black.png"
            alt=""
            class="inline mr-3 mb-3 w-4"
          />
          <p class="inline">3 > 6 members have booked</p>
        </div>
        <div>
          <img
            src="../../assets/imgs/buddie-blue.png"
            alt=""
            class="inline mr-3 mb-3 w-4"
          />
          <p class="inline">7 > members have booked</p>
        </div>
      </div>
    </div>

    <!-- Desktop Colour Codes Help Btn & Modal -->
    <div>
      <button
        class="
          hidden
          bg-[#FAFAFA]
          rounded-tl-lg rounded-br-lg
          h-7
          mr-5
          text-sm
          lg:flex
          items-center
          pr-5
          hover:bg-[#F4F4F4]
        "
        @click="
          showColourCodeHelp = !showColourCodeHelp;
          showIndicatorHelp = false;
        "
      >
        <div
          class="
            bg-meeow-primary
            rounded-tl-lg rounded-br-lg
            w-3
            h-7
            inline-block
            mr-5
          "
        ></div>
        Colour codes explained
      </button>

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
          top-[80%]
          -ml-[3%]
          z-50
        "
        v-if="showColourCodeHelp"
        @click="showColourCodeHelp = false"
      >
        <p class="mb-3">
          These colour codes tell you what type of Meeow you're seeing.
        </p>
        <div class="flex items-center mb-3">
          <div
            class="
              bg-meeow-primary
              rounded-tl-lg rounded-br-lg
              w-7
              h-7
              inline-block
              mr-3
            "
          ></div>
          <p class="inline">On-demand networking booking</p>
        </div>
        <div class="flex items-center mb-3">
          <div
            class="
              bg-[#9231CE]
              rounded-tl-lg rounded-br-lg
              w-7
              h-7
              inline-block
              mr-3
            "
          ></div>
          <p class="inline">A Meeow you've booked</p>
        </div>
        <div class="flex items-center mb-3">
          <div
            class="
              bg-[#00DCDC]
              rounded-tl-lg rounded-br-lg
              w-7
              h-7
              inline-block
              mr-3
            "
          ></div>
          <p class="inline">A Meeow you've created</p>
        </div>
      </div>
    </div>

    <!-- Search -->
    <input
      type="text"
      placeholder="Search for subjects and people"
      class="
        w-max
        placeholder:text-black
        px-6
        py-2
        flex-1
        lg:rounded-full lg:border-2 lg:border-black
      "
    />
    <i
      class="
        fa-solid fa-circle-xmark
        text-[#D8D8D8]
        mr-2
        lg:relative lg:-left-16
      "
    ></i>
    <button
      class="
        bg-black
        text-white
        h-[55px]
        w-[55px]
        lg:relative lg:-left-16 lg:rounded-full lg:h-9 lg:w-9
      "
    >
      <i class="fa-solid fa-magnifying-glass"></i>
    </button>

    <!-- Create Meeow Btn -->
    <button
      class="
        hidden
        lg:inline-block
        bg-black
        text-white text-sm
        rounded-full
        -ml-10
        px-7
        py-3
      "
    >
      Create a Meeow
    </button>
  </div>
</template>

<script>
export default {
  name: "SearchBar",
  data() {
    return {
      showIndicatorHelp: false,
      showColourCodeHelp: false,
    };
  },
};
</script>