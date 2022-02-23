<template>
  <div class="flex flex-col items-center gap-1">
    <div
      class="rounded-full bg-gradient-to-bl from-red-500 to-yellow-500 w-full h-auto"
    >
      <div class="m-0.5 bg-white rounded-full">
        <img
          class="h-auto p-0.5 rounded-full"
          :style="{ height: '72px' }"
          :src="require('~/assets/images/' + data.avatar)"
          alt=""
        />
      </div>
    </div>
    <p class="text-sm text-center w-full truncate">{{ data.username }}</p>
  </div>
</template>

<script>
export default {
  name: "Stories",
  props: {
    data: {
      type: Object,
      required: true,
    },
  },
};
</script>
