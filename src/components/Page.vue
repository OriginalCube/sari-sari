<script lang="ts">
import Search from "./Search.vue";
import CartItem from "./CartItem.vue";
import { foods } from "../Item.json";
export default {
  name: "Page",
  data() {
    return {
      items: foods,
    };
  },
  methods: {
    addItem(e: any) {
      this.$emit("addItem", e);
    },
  },
  components: { Search, CartItem },
};
</script>

<template>
  <div class="w-5/6 flex flex-col gap-4">
    <Search />
    <div
      class="h-80 w-full flex flex-wrap gap-10 p-4 items-center justify-evenly"
    >
      <CartItem
        @addItem="addItem"
        v-for="(items, index) in items"
        :key="index"
        :name="items.name"
        :price="items.price"
        :type="items.type"
      />
    </div>
  </div>
</template>

<style></style>
