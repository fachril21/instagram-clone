<template>
  <div class="w-full fixed top-0 h-14 shadow-md bg-white">
    <div class="container mx-auto px-3 flex items-center h-full">
      <div id="logo" class="w-40">
        <img src="~/assets/images/instagram.png" alt="" />
      </div>
      <div id="appbar-action" class="w-full flex flex-row gap-5 justify-end">
        <img src="~/assets/icons/home.svg" alt="home" />
        <img src="~/assets/icons/messenger.svg" alt="messenger" />
        <img src="~/assets/icons/new-post.svg" alt="new-post" />
        <img src="~/assets/icons/explore.svg" alt="explore" />
        <img src="~/assets/icons/activity.svg" alt="activity" />
        <div id="profile">
          <img
            class="w-auto rounded-full"
            :style="{ height: '24px' }"
            src="~/assets/images/ava-1.png"
            alt="ava-1"
          />
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "Appbar",
};
</script>
