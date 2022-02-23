<template>
  <div class="bg-white">
    <div
      id="header"
      class="w-full p-3 flex flex-row justify-between items-center"
    >
      <div class="flex flex-row gap-3 items-center">
        <div
          id="avatar"
          class="rounded-full bg-gradient-to-bl from-red-500 to-yellow-500 h-auto"
        >
          <div class="m-0.5 bg-white rounded-full">
            <img
              class="h-auto p-0.5 rounded-full"
              :style="{ height: '48px' }"
              :src="require('~/assets/images/' + post.avatar)"
              alt=""
            />
          </div>
        </div>

        <div id="username" class="font-medium">
          <span>
            {{ post.username }}
          </span>
        </div>
      </div>
      <div class="p-2 flex items-center justify-center">
        <i class="bx bx-dots-vertical-rounded"></i>
      </div>
    </div>

    <div id="image" class="w-full h-auto">
      <img
        class="h-auto"
        :src="require('~/assets/images/' + post.image)"
        alt=""
      />
    </div>

    <div id="action" class="flex flex-row justify-between p-3">
      <div class="flex flex-row gap-4">
        <img src="~/assets/icons/activity.svg" alt="" />
        <img src="~/assets/icons/comment.svg" alt="" />
        <img src="~/assets/icons/share.svg" alt="" />
      </div>
      <div>
        <img src="~/assets/icons/save.svg" alt="" />
      </div>
    </div>

    <div id="likes" class="px-3 py-1">
      <span class="font-medium">{{ post.likes }} likes</span>
    </div>

    <div id="username-desc" class="break-words px-3 py-1">
      <span class="line-clamp-2">
        <span class="font-medium">{{ post.username }}</span>
        <span ref="desc">
          {{ post.description }}
        </span>
      </span>
    </div>

    <div
      id="time"
      class="px-3 pt-2 pb-6 uppercase text-xs text-gray-300 font-medium"
    >
      {{ time }}
    </div>
  </div>
</template>

<script>
export default {
  name: "Post",
  props: {
    post: {
      type: Object,
      required: true,
    },
  },
  mounted() {},
  computed: {
    time() {
      var msPerMinute = 60 * 1000;
      var msPerHour = msPerMinute * 60;
      var msPerDay = msPerHour * 24;
      var msPerMonth = msPerDay * 30;
      var msPerYear = msPerDay * 365;

      var elapsed = new Date() - new Date(this.post.timestamp);

      if (elapsed < msPerMinute) {
        return Math.round(elapsed / 1000) + " seconds ago";
      } else if (elapsed < msPerHour) {
        return Math.round(elapsed / msPerMinute) + " minutes ago";
      } else if (elapsed < msPerDay) {
        return Math.round(elapsed / msPerHour) + " hours ago";
      } else if (elapsed < msPerMonth) {
        return "approximately " + Math.round(elapsed / msPerDay) + " days ago";
      } else if (elapsed < msPerYear) {
        return (
          "approximately " + Math.round(elapsed / msPerMonth) + " months ago"
        );
      } else {
        return (
          "approximately " + Math.round(elapsed / msPerYear) + " years ago"
        );
      }
    },
  },
};
</script>
