<template>
  <div class="bg-gray-100">
    <div class="w-full my-4" v-for="item in posts" :key="item.id">
      <post :post="item" />
    </div>
  </div>
</template>

<script>
import Post from "./Post.vue";
export default {
  components: { Post },
  name: "PostList",
  props: {
    posts: {
      type: Array,
      required: true,
    },
  },
};
</script>
