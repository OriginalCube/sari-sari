<script lang="ts">
import CartDetails from "./CartDetails.vue";
export default {
  name: "Cart",
  props: {
    cart: Array,
  },
  components: {
    CartDetails,
  },
  methods: {
    removeItem(e: any) {
      this.$emit("removeItem", e);
    },
  },
};
</script>

<template>
  <div class="w-1/6 h-auto flex flex-col gap-2 p-2 mt-24 rounded-md">
    <p class="text-3xl font-semibold">Reciept:</p>
    <input
      class="outline-none p-2"
      type="text"
      name=""
      placeholder="Enter name"
    />
    <p class="text-xl">Cart Items</p>
    <div class="w-5/6 h-60 overflow-y-auto">
      <CartDetails
        @removeItem="removeItem"
        :key="cart.id"
        v-for="cart in cart"
        :name="cart.name"
        :price="cart.price"
        :id="cart.id"
      />
    </div>
    <button
      class="p-2 bg-slate-800 rounded-md text-white border-2 border-slate-800 hover:text-slate-800 hover:bg-white"
    >
      Checkout
    </button>
  </div>
</template>

<style></style>
