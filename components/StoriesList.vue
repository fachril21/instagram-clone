<template>
  <div class="flex overflow-x-auto">
    <div class="flex flex-row gap-3 py-4 px-3">
      <div
        id="my-stories"
        class="flex flex-col items-center gap-1"
        :style="{ width: '74px' }"
      >
        <div
          class="rounded-full bg-gradient-to-bl from-red-500 to-yellow-500 w-full h-auto relative"
        >
          <div
            class="w-6 h-6 absolute bottom-0 right-0 bg-blue-500 border-2 border-white flex items-center justify-center rounded-full"
          >
            <i class="bx bx-plus text-white text-sm"></i>
          </div>
          <div class="m-0.5 bg-white rounded-full">
            <img
              class="h-auto p-0.5 rounded-full"
              :style="{ height: '72px' }"
              src="~/assets/images/ava-1.png"
              alt=""
            />
          </div>
        </div>
        <p class="text-sm text-center w-full truncate">Your story</p>
      </div>
      <div
        class="flex flex-col items-center gap-1"
        :style="{ width: '74px' }"
        v-for="item in stories"
        :key="item.id"
      >
        <div
          class="rounded-full bg-gradient-to-bl from-red-500 to-yellow-500 w-full h-auto"
        >
          <div class="m-0.5 bg-white rounded-full">
            <img
              class="h-auto p-0.5 rounded-full"
              :style="{ height: '72px' }"
              :src="require('~/assets/images/' + item.avatar)"
              alt=""
            />
          </div>
        </div>
        <p class="text-sm text-center w-full truncate">{{ item.username }}</p>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "StoriesList",
  props: {
    stories: {
      type: Array,
      required: true,
    },
  },
};
</script>
