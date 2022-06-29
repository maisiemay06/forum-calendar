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
    <!-- Date Picker -->
    <a href=""><i class="fa-solid fa-chevron-left mr-5"></i></a>
    <p class="text-[15px] mr-5">January 2022</p>
    <a href=""><i class="fa-solid fa-chevron-right mr-5"></i></a>
    <button
      class="
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

    <!-- Help Btns -->
    <button
      class="bg-meeow-light px-5 h-7 rounded-tl-lg rounded-br-lg mr-5 text-sm"
    >
      <img
        src="../../assets/imgs/buddie-blue.png"
        alt="blue book buddie"
        class="inline mr-1"
      />
      What do these mean?
    </button>
    <button
      class="
        bg-meeow-light
        rounded-tl-lg rounded-br-lg
        h-7
        mr-5
        text-sm
        flex
        items-center
        pr-5
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
};
</script>