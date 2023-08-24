<script lang="ts">
export default {
  name: "CartItem",
  props: {
    name: String,
    price: Number,
    type: String,
  },
  methods: {
    handleBuy() {
      const createItem = {
        id: Math.floor(Math.random() * 10000),
        name: this.name,
        price: this.price,
        type: this.type,
      };
      this.$emit("addItem", createItem);
    },
  },
};
</script>

<template>
  <div
    class="h-48 w-auto flex flex-col gap-1 border-2 border-slate-800 rounded-md overflow-hidden"
  >
    <div class="h-32 w-auto">
      <img
        class="h-full w-auto"
        src="https://media.tenor.com/gNnMMRunAq4AAAAC/ai-hoshino-hoshino-ai.gif"
        alt=""
      />
    </div>
    <div class="flex items-center justify-around gap-2">
      <div class="flex flex-col p-2">
        <p class="text-md font-semibold">{{ name }}</p>
        <p class="text-sm font-medium">₱ {{ price }}</p>
      </div>
      <img
        @click="handleBuy"
        src="/assets/icons/shopping-cart.png"
        class="h-6 w-auto cursor-pointer"
        alt=""
      />
    </div>
  </div>
</template>

<style></style>
