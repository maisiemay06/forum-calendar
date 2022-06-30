<template>
  <!-- Main Nav -->

  <div
    class="
      w-full
      flex
      justify-between
      items-end
      lg:items-center
      px-6
      pb-5
      lg:px-20 lg:pt-5 lg:pb-5
      border-b
      bg-white
      h-[90px]
    "
  >
    <!-- Logo -->
    <img
      src="../../assets/imgs/meeow-logo.png"
      alt="Meeow logo"
      class="h-[18px] w-auto mr-auto lg:mr-4"
    />
    <!-- Desktop Buttons -->
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
    <!-- Desktop Icons -->
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
    <div class="hidden lg:inline-block mr-12 group">
      <img
        src="../../assets/imgs/users-icon.png"
        alt="users icon"
        class="h-7"
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
          top-15
          -ml-10
          group-hover:visible
        "
        >My Meeows</span
      >
    </div>
    <!-- Favourites -->
    <div class="hidden lg:inline-block mr-12 group">
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
    <!-- Notifications -->
    <div class="hidden lg:inline-block mr-12 group">
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
          -ml-12
          group-hover:visible
        "
        >Notifications</span
      >
    </div>
    <!-- Connections -->
    <div class="hidden lg:inline-block mr-12 group">
      <img
        src="../../assets/imgs/connections-icon.png"
        alt="connections icon"
        class="h-5"
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
    <div class="hidden lg:inline-block mr-12 group">
      <img
        src="../../assets/imgs/message-icon.png"
        alt="message icon"
        class="h-5"
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
        >Messaging</span
      >
    </div>

    <!-- Profile Img -->
    <img
      src="../../assets/imgs/user-img-1.png"
      alt="user profile img"
      class="
        hidden
        lg:inline-block
        rounded-tl-lg rounded-br-lg
        w-[58px]
        h-[58px]
        hover:cursor-pointer
      "
    />

    <!-- Mobile Create Meeow Btn -->
    <button
      class="
        inline-block
        lg:hidden
        bg-meeow-primary
        rounded-full
        px-5
        py-1
        text-white text-[15px]
      "
    >
      Create a Meeow
    </button>
  </div>
</template>

<script>
export default {
  name: "MainNav",
  props: ["openModal"],
};
</script>