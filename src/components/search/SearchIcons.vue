<script lang="ts">
export default {
  name: "SearchIcons",
  props: {
    name: String,
    image: String,
  },
  methods: {
    getImage(src: string) {
      return `/assets/icons/${src}.png`;
    },
  },
};
</script>

<template>
  <div
    class="w-auto h-16 border-black rounded-md flex items-center justify-center gap-2 p-4 cursor-pointer"
  >
    <img class="h-full w-auto" :src="getImage(image)" alt="" />
    <p class="text-md">{{ name }}</p>
  </div>
</template>

<style></style>
