<script lang="ts">
import Page from "./components/Page.vue";
import Cart from "./components/Cart.vue";

export default {
  name: "App",
  data() {
    // 6 types of foods
    return {
      price: 0,
      cart: [],
      user: {
        name: "",
        number: 0,
      },
    };
  },
  methods: {
    addItem(e: any) {
      this.cart = [...this.cart, e];
    },
    removeItem(e: any) {
      this.cart = this.cart.filter((el: any) => el.id !== e);
    },
  },
  components: {
    Page,
    Cart,
  },
};
</script>

<template>
  <div class="p-4 w-full h-auto flex justify-around gap-4">
    <Page @addItem="addItem" />
    <Cart :cart="cart" @removeItem="removeItem" />
  </div>
</template>
