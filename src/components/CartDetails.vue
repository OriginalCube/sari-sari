<script lang="ts">
export default {
  name: "CartDetails",
  props: {
    name: String,
    price: Number,
    id: Number,
  },
  methods: {
    removeItem() {
      this.$emit("removeItem", this.id);
    },
  },
};
</script>

<template>
  <div class="w-full h-auto flex items-center justify-between gap-4 p-2">
    <p class="text-xl font-medium">{{ name }}</p>
    <div class="h-auto w-auto flex items-center justify-evenly gap-2">
      <p class="text-xl">₱ {{ price }}</p>
      <img
        @click="removeItem"
        src="/assets/icons/p.png"
        class="h-4 w-auto cursor-pointer"
        alt=""
      />
    </div>
  </div>
</template>

<style></style>
