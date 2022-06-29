<template>
  <!-- Main Nav -->

  <div
    class="
      w-full
      flex
      justify-between
      items-center
      px-6
      pb-3
      lg:px-20 lg:pt-5 lg:pb-5
      border-b
      bg-white
      h-[100px]
      lg:h-[90px]
    "
  >
    <!-- Logo -->
    <img
      src="../../assets/imgs/meeow-logo.png"
      alt="Meeow logo"
      class="h-[18px] w-auto mr-auto lg:mr-4"
    />
    <!-- Buttons -->
    <a
      href=""
      class="
        hidden
        lg:inline-block
        text-[15px]
        bg-transparent
        rounded-full
        px-8
        py-3
        hover:bg-[#F4F4F4]
        transition
        duration-300
        ease-in
      "
      >How Meeow works</a
    >
    <a
      href=""
      class="
        hidden
        lg:inline-block
        text-[15px]
        bg-transparent
        rounded-full
        px-7
        py-3
        hover:bg-[#F4F4F4]
        transition
        duration-300
        ease-in
        mr-auto
      "
      >Browse Subjects</a
    >
    <!-- Icons -->
    <!-- Points -->
    <div class="hidden lg:inline-block mr-12 group">
      <div class="inline relative -top-4">
        <p class="text-[15px] inline mr-1">Captain</p>
        <p class="bg-black text-white rounded-full text-xs inline p-1">
          50,258
        </p>
      </div>
      <i
        class="fa-solid fa-star text-xl inline"
        @click="() => openModal('points')"
      ></i>
      <span
        class="
          bg-black
          text-white
          rounded-full
          invisible
          px-2
          py-1
          text-xs
          absolute
          top-14
          -ml-9
          group-hover:visible
        "
        >Points</span
      >
    </div>
    <!-- My Meeows -->
    <div class="mr-12 group">
      <img src="../../assets/imgs/users-icon.png" alt="users icon" />
      <span
        class="
          bg-black
          text-white
          rounded-full
          invisible
          px-2
          py-1
          text-xs
          absolute
          top-14
          -ml-10
          group-hover:visible
        "
        >My Meeows</span
      >
    </div>
    <!-- Favourites -->
    <div class="mr-12 group">
      <i class="fa-solid fa-heart text-xl"></i>
      <span
        class="
          bg-black
          text-white
          rounded-full
          invisible
          px-2
          py-1
          text-xs
          absolute
          top-14
          -ml-11
          group-hover:visible
        "
        >Favourites</span
      >
    </div>
    <!-- Meeow -->
    <div class="mr-12 group">
      <i class="fa-solid fa-bell text-xl"></i>
      <span
        class="
          bg-black
          text-white
          rounded-full
          invisible
          px-2
          py-1
          text-xs
          absolute
          top-14
          -ml-9
          group-hover:visible
        "
        >Meeow</span
      >
    </div>
    <!-- Connections -->
    <div class="mr-12 group">
      <img
        src="../../assets/imgs/connections-icon.png"
        alt="connections icon"
      />
      <span
        class="
          bg-black
          text-white
          rounded-full
          invisible
          px-2
          py-1
          text-xs
          absolute
          top-14
          -ml-10
          group-hover:visible
        "
        >Connections</span
      >
    </div>
    <!-- Calendar -->
    <div class="hidden lg:inline-block mr-12 group">
      <i class="fa-solid fa-calendar text-xl"></i>
      <span
        class="
          bg-black
          text-white
          rounded-full
          invisible
          px-2
          py-1
          text-xs
          absolute
          top-14
          -ml-10
          group-hover:visible
        "
        >Calendar</span
      >
    </div>
    <!-- Messaging -->
    <div class="mr-12 group">
      <img src="../../assets/imgs/message-icon.png" alt="message icon" />
      <span
        class="
          bg-black
          text-white
          rounded-full
          invisible
          px-2
          py-1
          text-xs
          absolute
          top-14
          -ml-12
          group-hover:visible
        "
        >Messaging</span
      >
    </div>

    <!-- Profile Img -->
    <img
      src="../../assets/imgs/user-img-1.png"
      alt="user profile img"
      class="rounded-tl-lg rounded-br-lg w-[58px] h-[58px] hover:cursor-pointer"
    />

    <!-- Mobile Burger Menu -->
    <i
      class="fa-solid fa-ellipsis-vertical text-3xl ml-4 lg:hidden"
      @click="toggleNavMenu"
    ></i>
  </div>

  <!-- Mobile Nav Menu -->
  <div
    v-if="showNavMenu"
    class="
      z-20
      absolute
      bg-white
      right-0
      h-[100vh]
      w-2/3
      drop-shadow-xl
      pt-28
      pl-10
      text-left
      flex flex-col
      items-start
      text-lg
    "
  >
    <ul>
      <li class="py-3">Favourites</li>
      <li class="py-3">Calendar</li>
      <li class="py-3">Messaging</li>
      <li class="py-3">Tell a Friend</li>
      <li class="py-3">Points</li>
    </ul>
    <button class="mt-auto pb-10 flex items-center" @click="toggleNavMenu">
      Close <i class="fa-solid fa-xmark text-3xl ml-2"></i>
    </button>
  </div>
</template>

<script>
export default {
  name: "MainNav",
  props: ["openModal"],
};
</script>