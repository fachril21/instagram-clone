<template>
  <div class="pt-14">
    <div class="">
      <stories-list :stories="stories" />
    </div>
  </div>
</template>

<script>
import StoriesList from "~/components/StoriesList.vue";
export default {
  components: { StoriesList },
  data() {
    return {
      stories: [
        {
          id: 1,
          username: "johndoe",
          avatar: "ava-2.png",
        },
        {
          id: 2,
          username: "zachreimund",
          avatar: "ava-3.png",
        },
        {
          id: 3,
          username: "sabihaball",
          avatar: "ava-4.png",
        },
        {
          id: 4,
          username: "caitlin",
          avatar: "ava-5.png",
        },
        {
          id: 5,
          username: "tonicha",
          avatar: "ava-6.png",
        },
        {
          id: 6,
          username: "manhagreer",
          avatar: "ava-7.png",
        },
      ],
    };
  },
};
</script>
