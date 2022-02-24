<template>
  <div class="pt-14">
    <stories-list :stories="stories" />
    <post-list :posts="posts" />
  </div>
</template>

<script>
import PostList from "~/components/PostList.vue";
import StoriesList from "~/components/StoriesList.vue";
export default {
  components: { StoriesList, PostList },
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
      posts: [
        {
          id: 1,
          username: "manhagreer",
          avatar: "ava-7.png",
          image: "post-1.jpg",
          description:
            "long long long long long long long long long long long long long long long long long long journey 🚗",
          likes: 84,
          timestamp:
            "Wed Feb 24 2022 11:58:30 GMT+0700 (Western Indonesia Time)",
        },
        {
          id: 2,
          username: "tonicha",
          avatar: "ava-6.png",
          image: "post-2.jpg",
          description: "long long long journey 🚗",
          likes: 84,
          timestamp:
            "Wed Feb 24 2022 09:58:30 GMT+0700 (Western Indonesia Time)",
        },
        {
          id: 3,
          username: "caitlin",
          avatar: "ava-5.png",
          image: "post-3.jpg",
          description: "long long long journey 🚗",
          likes: 84,
          timestamp:
            "Wed Feb 24 2022 07:58:30 GMT+0700 (Western Indonesia Time)",
        },
        {
          id: 4,
          username: "sabihaball",
          avatar: "ava-4.png",
          image: "post-4.jpg",
          description: "long long long journey 🚗",
          likes: 84,
          timestamp:
            "Wed Feb 23 2022 12:58:30 GMT+0700 (Western Indonesia Time)",
        },
        {
          id: 5,
          username: "zachreimund",
          avatar: "ava-3.png",
          image: "post-5.jpg",
          description: "long long long journey 🚗",
          likes: 84,
          timestamp:
            "Wed Feb 23 2022 10:58:30 GMT+0700 (Western Indonesia Time)",
        },
        {
          id: 6,
          username: "johndoe",
          avatar: "ava-2.png",
          image: "post-6.jpg",
          description: "long long long journey 🚗",
          likes: 84,
          timestamp:
            "Wed Feb 22 2022 19:58:30 GMT+0700 (Western Indonesia Time)",
        },
        {
          id: 7,
          username: "levvs",
          avatar: "ava-1.png",
          image: "post-7.jpg",
          description: "long long long journey 🚗",
          likes: 84,
          timestamp:
            "Wed Feb 21 2022 19:58:30 GMT+0700 (Western Indonesia Time)",
        },
      ],
    };
  },
};
</script>
